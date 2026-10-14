# 11. Coding and data structures

97 questions. Sources are tagged per question. Full answers are in the linked source repo.

---

11.001  Implement scaled dot-product attention with a causal mask, from scratch, in NumPy or PyTorch.
> Asked at: Amazon, Anthropic, Google DeepMind | Source: Company-wise (pallavi-shekhar)

11.002  Implement multi-head attention, then convert it to grouped-query attention.
> Asked at: Alibaba, Google DeepMind, Mistral AI | Source: Company-wise (pallavi-shekhar)

11.003  Implement a KV cache and single-step decode.
> Asked at: Moonshot AI | Source: Company-wise (pallavi-shekhar)

11.004  Implement BPE training and encoding from scratch.
> Asked at: Coding and Data Structures | Source: Company-wise (pallavi-shekhar)

11.005  Implement top-k, top-p and temperature sampling over a logits vector.
> Asked at: Apple, Google DeepMind | Source: Company-wise (pallavi-shekhar)

11.006  Implement an LRU cache with O(1) get/put, then add TTL.
> Asked at: Alibaba, OpenAI, xAI | Source: Company-wise (pallavi-shekhar)

11.007  Implement a token-bucket rate limiter, then make it distributed.
> Asked at: Anthropic, Cohere, OpenAI, xAI | Source: Company-wise (pallavi-shekhar)

11.008  Write an async batch processor over an API with concurrency limits, retries with jitter and error isolation.
> Asked at: Anthropic, Perplexity | Source: Company-wise (pallavi-shekhar)

11.009  Write a streaming SSE/JSON parser that handles arbitrary chunk boundaries.
> Asked at: Cohere | Source: Company-wise (pallavi-shekhar)

11.010  Implement a text chunker with overlap that never splits a semantic unit.
> Asked at: Harvey | Source: Company-wise (pallavi-shekhar)

11.011  Implement cosine similarity search over embeddings, then explain why you would not ship it.
> Asked at: Coding and Data Structures | Source: Company-wise (pallavi-shekhar)

11.012  Implement a minimal agent loop with tool dispatch, error handling and a step budget.
> Asked at: Cognition | Source: Company-wise (pallavi-shekhar)

11.013  Build core business logic for a toy banking application: a spec that grows in four progressive levels against a black-box evaluator.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.014  Build an in-memory database: SET/GET/DELETE first, then filtered scans, then TTL with timestamps, then file compaction.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.015  Create a task scheduler.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.016  Build an OOP system for managing courses, grades and students.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.017  Given a helper method that crawls a URL, write a crawler over a domain: first synchronous, then make it async.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.018  Convert nested stack traces into discrete start and end events.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.019  Build a rate limiter. Every ten minutes I add a requirement: per-tenant limits, burst allowances, then a sliding window. How do you keep the code from collapsing?
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.020  You need to run an LLM call over 50,000 documents. The API allows ~100 concurrent requests and occasionally returns 429s and timeouts. Write the Python.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.021  How would you parallelise this task? (Concurrency and data mutation come up repeatedly across rounds.)
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.022  SQL: write a query to find the top five pairs of products most frequently purchased together.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.023  SQL: determine whether any user has overlapping subscription date ranges.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.024  SQL: return each employee's current salary after an ETL error inserted a new salary row every year.
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

11.025  Design and implement an in-memory key-value store supporting set, transactional begin, commit and abort.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.026  Create a database ORM, step by step.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.027  Code a trivial web crawler using Go.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.028  Implement a UI from a mockup with provided CSS and API.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.029  Refactor bad code: here are ~120 lines of working but messy code with passing tests. Improve the architecture without breaking them. What do you change first?
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.030  Write a Python function that displays the first n Fibonacci numbers.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.031  Infection-spread simulation.
> Asked at: OpenAI | Source: Company-wise (pallavi-shekhar)

11.032  You are receiving an unbounded stream of event IDs. Return the k most frequent IDs seen so far, at any point, with bounded memory.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

11.033  Closest key: given a dictionary with letter keys and lists of letters as values, find the closest key.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

11.034  Write a function to compute root-mean-square error given y_pred and y_true lists.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

11.035  Parse bigrams: extract two-word phrases from strings for NLP feature engineering.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

11.036  Given an array nums of n integers where n > 1, return an output array (product of array except self).
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.037  Find the minimum window in S which will contain all the characters in T.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.038  Serialize and deserialize a binary tree.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.039  Convert a binary tree to a circular doubly linked list.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.040  Alien dictionary: determine character ordering from a sorted word list.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.041  K closest points to origin; top-k frequent elements; minimum number of conference rooms.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.042  Regular expression matching with '.' and '\*'.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.043  Two-part warm-up: given a stream of user actions, return the k most engaged-with items. Then: why might your heap solution be the wrong choice in production?
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

11.044  Build an in-memory key-value store with SET/GET/DELETE, then add transactions with BEGIN/COMMIT/ROLLBACK, including nested transactions.
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

11.045  Write an iterator class that lazily flattens an arbitrarily nested list of lists/integers: no generators, explicit state.
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

11.046  Here is a scheduler class from a small LLM inference engine. One method, \_admit_requests, is a stub: no spec, no docstring, no tests. Walk me through your first thirty minutes.
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

11.047  Pair-programming: build a service that takes a user question, enriches it with data from a third-party API, and answers via a chat-model API. How do you structure it?
> Asked at: Mistral AI | Source: Company-wise (pallavi-shekhar)

11.048  Design a token-based rate limiter for a multi-tenant LLM API. Implement the core, then tell me what changes when it's distributed.
> Asked at: Cohere | Source: Company-wise (pallavi-shekhar)

11.049  Qwen2.5-Coder trains with repository-level fill-in-the-middle using tokens like <|fim_prefix|>, <|fim_suffix|>, <|repo_name|>. Write the function that formats a repo-level FIM example, and explain why repo-level beats file-level.
> Asked at: Alibaba | Source: Company-wise (pallavi-shekhar)

11.050  Write code to measure a tokenizer's fertility across languages, and explain what you would do with the result.
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

11.051  Implement “top-k most frequent search queries” over a large query log, then tell me what breaks when the log becomes an unbounded stream across many machines.
> Asked at: Microsoft | Source: Company-wise (pallavi-shekhar)

11.052  Low-level design: sketch the classes and interfaces for the tool-calling layer of an agent host, where tools can come from native code, an OpenAPI spec, or an MCP server.
> Asked at: Microsoft | Source: Company-wise (pallavi-shekhar)

11.053  Find the top-K most frequent items in a high-volume event stream with bounded memory.
> Asked at: Amazon | Source: Company-wise (pallavi-shekhar)

11.054  Divide two integers without using multiplication, division or modulo. Find the number of connected components in a graph. Check balanced parentheses.
> Asked at: Amazon | Source: Company-wise (pallavi-shekhar)

11.055  Here's a CUDA kernel that's 10x slower than expected. Without running it, what are the usual suspects, and how do you confirm each?
> Asked at: NVIDIA | Source: Company-wise (pallavi-shekhar)

11.056  Implement the block manager for a paged KV cache: allocate, append, free, and copy-on-write prefix sharing.
> Asked at: NVIDIA | Source: Company-wise (pallavi-shekhar)

11.057  A model runs fine in FP32 but produces garbage after conversion to FP16. Debug it.
> Asked at: NVIDIA | Source: Company-wise (pallavi-shekhar)

11.058  Implement non-maximum suppression. Then vectorise it.
> Asked at: Tesla | Source: Company-wise (pallavi-shekhar)

11.059  Write an efficient ring buffer for high-rate sensor data with a fixed memory budget.
> Asked at: Tesla | Source: Company-wise (pallavi-shekhar)

11.060  Implement a streaming top-k with a bounded-memory sketch; implement a sliding-window rate counter.
> Asked at: Consumer-Scale ML Companies | Source: Company-wise (pallavi-shekhar)

11.061  Implement a thread-safe batching logger: many producer threads call log(msg); a background thread flushes batches of up to 100 messages every second or when full.
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

11.062  You have a stream of billions of events and need the top-K most frequent keys with bounded memory. Exact is impossible: what do you do?
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

11.063  Given allowed IP ranges as CIDR blocks plus explicit deny ranges, implement is_allowed(ip) efficiently for millions of checks per second.
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

11.064  A Spark job joining a 2 TB fact table to a 50 GB dimension table has one straggler task running 100x longer than the rest. Diagnose and fix it.
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

11.065  A Structured Streaming job reads Kafka and writes to a Delta table. The cluster is killed mid-batch and restarts. Does the customer get duplicate rows? Explain at the level of the checkpoint and the transaction log.
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

11.066  Our compiler statically schedules every instruction and every chip-to-chip transfer. What does that compiler need to know that an NVCC-style compiler does not, and what breaks when it's wrong?
> Asked at: Groq | Source: Company-wise (pallavi-shekhar)

11.067  Design the IR and pass pipeline for a compiler targeting a spatial dataflow accelerator. Where does the memory-residency decision live, and why?
> Asked at: Groq | Source: Company-wise (pallavi-shekhar)

11.068  Write the host-side runtime that feeds a deterministic accelerator across many chips. What is genuinely hard about it?
> Asked at: Groq | Source: Company-wise (pallavi-shekhar)

11.069  A model passes bit-exact against the functional simulator on one chip but produces wrong output at rack scale. How do you find it?
> Asked at: Groq | Source: Company-wise (pallavi-shekhar)

11.070  Write the server-side handler for streaming token generation. Handle client disconnects correctly.
> Asked at: Together AI | Source: Company-wise (pallavi-shekhar)

11.071  `transformers` famously repeats code: each model gets its own self-contained modeling file. Defend that decision, then critique it.
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

11.072  Why did Hugging Face create safetensors when pickle-based checkpoints already worked everywhere?
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

11.073  A user loads a 2 TB dataset with `datasets` on a 64 GB RAM machine and it works. How? And when does it stop working?
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

11.074  Build the task-lifecycle core of an annotation platform. Start simple; I'll add consensus of k annotators, then priority re-review, then annotator cooldowns.
> Asked at: Scale AI | Source: Company-wise (pallavi-shekhar)

11.075  Given annotation sessions as (start, end) timestamps, return the peak number of concurrent annotators and the intervals at peak load.
> Asked at: Scale AI | Source: Company-wise (pallavi-shekhar)

11.076  Implement a client pool over multiple LLM providers with failover: providers fail, time out, or rate-limit, and callers should just get a completion.
> Asked at: Perplexity | Source: Company-wise (pallavi-shekhar)

11.077  You're ingesting millions of web pages a day. Detect near-duplicates (same article, different boilerplate) efficiently.
> Asked at: Perplexity | Source: Company-wise (pallavi-shekhar)

11.078  You need to embed millions of text chunks. The embedding service takes batches with a max batch size and a max total-token limit. Write the batcher and make it fast.
> Asked at: Perplexity | Source: Company-wise (pallavi-shekhar)

11.079  Implement beam search for an autoregressive model. When would an answer engine actually use it?
> Asked at: Perplexity | Source: Company-wise (pallavi-shekhar)

11.080  Build a hash tree to organise data in a repository.
> Asked at: Cursor | Source: Company-wise (pallavi-shekhar)

11.081  Given a repository snapshot (path → content), build a Merkle tree and write the function returning which files changed between two snapshots without comparing every file's content.
> Asked at: Cursor | Source: Company-wise (pallavi-shekhar)

11.082  Print the top view of nodes in a binary tree.
> Asked at: Cursor | Source: Company-wise (pallavi-shekhar)

11.083  Find duplicate files in a file system.
> Asked at: Cursor | Source: Company-wise (pallavi-shekhar)

11.084  Implement the core of an editor text buffer: efficient insert/delete at arbitrary positions and fast line lookup. What structure do you pick?
> Asked at: Cursor | Source: Company-wise (pallavi-shekhar)

11.085  You're handed a small unfamiliar agent codebase. Users report it sometimes confirms an order that was never actually placed. How do you debug it?
> Asked at: Sierra | Source: Company-wise (pallavi-shekhar)

11.086  Paired coding: write a chunker for a legal document that never splits a clause and carries enough context that a retrieved chunk is self-contained.
> Asked at: Harvey | Source: Company-wise (pallavi-shekhar)

11.087  Merge ranked results from N connector shards into a global top-k, applying a per-user permission filter. Do it efficiently.
> Asked at: Glean | Source: Company-wise (pallavi-shekhar)

11.088  Live coding: build the prompt for the next turn under a fixed token budget. The catch is our prefix cache.
> Asked at: Character.AI | Source: Company-wise (pallavi-shekhar)

11.089  Write a service that proxies streaming TTS to a browser and cancels cleanly when the user navigates away.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

11.090  In NumPy, compute minADE and minFDE for multi-modal trajectory predictions with variable-length ground truth. No Python loops.
> Asked at: Waymo | Source: Company-wise (pallavi-shekhar)

11.091  Implement a set of shape classes that compute area, then extend them to handle a new shape.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.092  Write a SQL query that joins and aggregates across tables to answer a business question.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.093  Build a function that fetches paginated data from a REST API, handling page size and total-page logic.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.094  Find and fix a double-counting bug in a function that tallies values in a HashMap.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.095  Debug a program that models infection spread across a social graph.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.096  You inherit an 800-line pipeline script from a previous deployment. It's slow and occasionally produces wrong numbers. The original author is gone. Go.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

11.097  Given exports from three customer systems, each with its own customer records, write code to produce one deduplicated set of entities and explain your design.
> Asked at: Palantir | Source: Company-wise (pallavi-shekhar)

