# 15. Senior engineering gap-fill

The two AI sources are strong on LLM internals, RAG, agents and evaluation. They are thin on classic senior-engineering topics: architecture trade-offs, delivery pipelines, security fundamentals, estimation, code quality, and leadership. This section fills those gaps. The questions come from the topic list in [bmadone/senior-software-engineer](https://github.com/bmadone/senior-software-engineer). The answers are written for this bank, not copied from that repo, which only links to resources.

Each answer is a short key-point summary. Expand each one in your own words before an interview.

---

## Architecture and design

### 15.001 When would you choose a monolith over microservices?
Start with a monolith when the team is small, the domain boundaries are still moving, and deploy coupling is cheap to manage. Move to services when independent scaling, team ownership, or release cadence actually hurts. Microservices add network failure modes, distributed data, and operational overhead, so the split has to pay for them.

### 15.002 What does "separation of concerns" look like in a real service?
Keep transport (HTTP handlers), business rules, and persistence in separate layers. Business rules should not import the web framework or the ORM. This makes the rules testable without a server or database, and it lets you change the storage layer without touching the rules.

### 15.003 Explain dependency injection and when it helps.
Pass dependencies in (constructor or parameters) rather than having a class build them. This lets tests swap in fakes and lets the wiring live in one place. It helps most at module boundaries that need to vary, such as storage, external APIs, and clocks. It is overkill for small scripts.

### 15.004 Composition vs inheritance: which do you default to?
Default to composition. Inheritance couples a subclass to its parent's internals, and deep hierarchies are hard to change. Use inheritance only for a true "is-a" relationship with a stable contract.

### 15.005 What are SOLID principles, and which one do people misapply most?
Single responsibility, open/closed, Liskov substitution, interface segregation, and dependency inversion. The most misapplied is single responsibility. People split classes by technical layer or into one-method classes, which spreads one concept across many files without making it simpler. Split by reason to change instead.

### 15.006 What is an event-driven architecture, and what does it cost you?
Services publish events and others react, which decouples producers from consumers. The costs are eventual consistency, harder debugging across async hops, and the need for idempotent consumers and a way to replay. Use it for workflows where reacting later is acceptable.

### 15.007 When would you use a message queue instead of a direct API call?
When the caller does not need the result right away, when work can be retried, when load needs smoothing, or when one producer fans out to many consumers. A queue buys resilience and buffering. It costs latency and needs dead-letter handling and idempotency.

### 15.008 Explain the CAP theorem in practical terms.
During a network partition you must choose between consistency (every read sees the latest write) and availability (every request gets a response). Many systems are not picking one globally; they pick per operation. Name the trade-off for the specific data, not the database brand.

### 15.009 What is a circuit breaker and why use one?
A wrapper that stops calling a failing dependency after a threshold of errors, returns a fast failure or fallback, and retries after a cool-down. It stops one slow dependency from exhausting threads and cascading through the system.

### 15.010 Retries: what must you add before adding one?
Timeouts, bounded retries with exponential backoff and jitter, and idempotency on the operation. Without idempotency, a retry after a timeout can charge a customer twice. Retry only errors that can succeed on retry, such as 503 or timeouts, not 400.

### 15.011 Caching: what are the main strategies and their risks?
Cache-aside (read populates the cache, write invalidates), write-through, and write-behind. The hard part is invalidation and stale reads. Use TTLs as a safety net, and know which data can tolerate staleness.

### 15.012 What is a database index, and what does it cost?
A sorted or hashed structure that speeds reads on specific columns. It costs write latency, storage, and maintenance. Index the columns your queries filter and join on, and check the query plan before adding one.

### 15.013 What is database normalization, and when do you denormalize?
Normalization removes duplicated data so each fact lives in one place. Denormalize deliberately for read-heavy paths where joins are too expensive, and accept the cost of keeping copies in sync.

### 15.014 How do you handle a schema migration safely in production?
Use expand and contract. Add the new column or table, deploy code that writes both, backfill, switch reads, then remove the old column in a later release. Avoid long locks and never ship a change that breaks the currently deployed code.

---

## Performance

### 15.015 How do you find a performance bottleneck?
Measure first. Start with a profiler or traces, then check the database, then network calls, then the hot loop. Change one thing at a time and re-measure against a baseline. Guessing wastes effort.

### 15.016 What is the N+1 query problem?
Loading a list of N parents and then issuing one query per parent for a child relation. It is fixed with a join, a batch load, or an eager-load query. It hides in ORMs and only shows up under real data volumes.

### 15.017 What are Core Web Vitals, and which one replaced FID?
Largest Contentful Paint (loading), Interaction to Next Paint (responsiveness), and Cumulative Layout Shift (visual stability). INP replaced First Input Delay as the responsiveness metric in 2024.

### 15.018 Latency vs throughput: how do they differ?
Latency is how long one request takes. Throughput is how many requests complete per unit time. You can raise throughput with batching and concurrency while latency gets worse. State which one the product needs.

---

## Communication protocols

### 15.019 When would you choose gRPC over REST?
gRPC suits internal service-to-service calls that need strong typing, streaming, and low overhead, using HTTP/2 and protobuf. REST suits public APIs that need broad client support, caching by HTTP semantics, and easy debugging with a browser.

### 15.020 What is the difference between SSE and WebSockets?
Server-Sent Events are one-way, server-to-client, over plain HTTP, and reconnect automatically. WebSockets are full duplex. Use SSE for streaming LLM tokens or notifications. Use WebSockets when clients send frequent messages back.

### 15.021 What does idempotent mean for an HTTP method?
Repeating the request gives the same effect as sending it once. GET, PUT, and DELETE are defined as idempotent. POST is not, so payment or order creation needs an idempotency key.

---

## Code quality and testing

### 15.022 What does a good test pyramid look like?
Many fast unit tests, fewer integration tests against real dependencies, and a small number of end-to-end tests for critical flows. Inverting it gives slow, flaky suites.

### 15.023 What makes a test flaky, and how do you fix one?
Shared state, timing assumptions, real network calls, and test order dependence. Remove the randomness or timing, isolate state, fake the external service, and quarantine any test you cannot fix quickly.

### 15.024 What do you look for in a code review?
Correctness and edge cases first, then security and failure handling, then tests, then readability and naming. Keep feedback about the code, not the author, and separate blocking issues from suggestions.

### 15.025 When is a refactor worth doing before a feature?
When the change would otherwise copy or tangle existing logic, and the refactor is covered by tests. Refactor in a separate change from behavior changes so each diff is easy to review.

---

## CI/CD and delivery

### 15.026 What belongs in a CI pipeline for a service?
Lint and type checks, unit tests, build, security scans (dependencies and secrets), integration tests, and an artifact published with a version. Fail fast: cheap checks run first.

### 15.027 What is GitOps?
The desired state of the system lives in git. A controller such as Argo CD or Flux reconciles the cluster to match it. Rollbacks become git reverts, and the audit trail is the commit history.

### 15.028 What is a canary deployment, and how do you decide to roll it back?
Send a small share of traffic to the new version and compare error rate, latency, and business metrics with the old version. Roll back automatically when the canary breaches the thresholds you set before the rollout.

### 15.029 What do SBOM, SLSA, and Sigstore address?
An SBOM lists the components in a build so you can find affected packages quickly. SLSA defines levels of build integrity and provenance. Sigstore signs artifacts and verifies signatures without managing long-lived keys. Together they make the supply chain verifiable.

### 15.030 What are the four DORA metrics?
Deployment frequency, lead time for changes, change failure rate, and time to restore service. They measure delivery performance together. Optimizing one alone, such as deploy count, can hurt the others.

---

## Security fundamentals

### 15.031 What are the most common web vulnerabilities an interviewer expects you to name?
Injection (SQL, command), broken access control, cross-site scripting, and vulnerable or outdated components. Also know cross-site request forgery and insecure deserialization, which were on earlier OWASP lists; the 2021 Top 10 folds deserialization into software and data integrity failures. Secrets in source are a common finding, though they aren't a separate OWASP category.

### 15.032 How do you prevent SQL injection?
Use parameterized queries or an ORM that binds parameters. Never build SQL by concatenating user input. Least-privilege database accounts limit the damage if it happens anyway.

### 15.033 Authentication vs authorization?
Authentication proves who the caller is. Authorization decides what that caller may do. Most access-control bugs are authorization bugs, where the check is missing on one endpoint or object.

### 15.034 Where should secrets live?
In a secrets manager or the platform's secret store, injected at runtime. Never in source control, and rotate them when someone with access leaves or a leak is suspected.

### 15.035 What is the principle of least privilege applied to a service?
Give each service identity only the permissions it uses, scoped to the resources it needs. Review grants when the code changes.

---

## Estimation and delivery process

### 15.036 How do you estimate a project that has a lot of unknowns?
Break it into the smallest deliverable pieces, estimate ranges rather than points, identify the riskiest unknowns, and spike them first. Track actuals to calibrate the next estimate.

### 15.037 What is technical debt, and how do you justify paying it down?
Debt is the cost of future change caused by present shortcuts. Justify it in terms of the business impact: how often the code changes, incidents it causes, and the time it adds to each feature.

### 15.038 How do you decide between build and buy?
Buy when the capability is undifferentiated and the vendor's cost is below the total cost of owning it. Build when it is core to the product or the requirements no vendor fits. Count maintenance, not just the initial work.

---

## Leadership, communication and behavior

### 15.039 Describe how you would handle a production incident.
Stabilize first (roll back or mitigate), communicate status to stakeholders on a regular cadence, then find the root cause after service is restored. Follow with a blameless postmortem that produces concrete action items with owners.

### 15.040 How do you influence a decision when you do not have authority?
Make the trade-off explicit with data, write the proposal down, invite the people who will be affected, and agree on how you will decide if you disagree. Commit to the outcome even if you lose the argument.

### 15.041 What does a senior engineer do that a mid-level engineer usually does not?
Frames ambiguous problems, anticipates failure modes, reduces the team's blockers, makes trade-offs visible, and raises the quality of other people's work through reviews and mentoring. Scope grows from the feature to the system and the team.

### 15.042 How do you use AI coding tools without losing engineering judgment?
Use them to speed up drafts, tests, and exploration, then review every change as if a junior wrote it. Verify with tests and read the code you ship. Keep ownership of design and trade-offs.

---

## Quick self-check

Answer these out loud without notes:

1. Walk through how a request passes through a service with a timeout, a retry, and a circuit breaker.
2. Name three ways a deployment can fail and what you would check first.
3. Explain why a retry on a POST can be dangerous, and what you would add.
4. Name the three Core Web Vitals and what each one measures.
