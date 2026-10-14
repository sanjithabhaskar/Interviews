# AI Engineering Interview Q&A Bank

A combined question bank for AI engineer and senior software engineer interviews. It merges three public sources, removes near-duplicate questions, tags each question with the companies that have been reported asking it, and fills the gaps with senior-engineering questions.

## Sources

| Source | What it contributed |
| --- | --- |
| [aishwaryanr/awesome-generative-ai-guide](https://github.com/aishwaryanr/awesome-generative-ai-guide/blob/main/interview_prep/roles/ai-engineer/questions.md) | 145 AI engineer questions across LLM fundamentals, RAG, agents, evaluation, cost, safety, and system design. Full answers are in the source. |
| [pallavi-shekhar/ai-engineering-interview-questions-company-wise](https://github.com/pallavi-shekhar/ai-engineering-interview-questions-company-wise) | About 600 questions reported at about 35 AI companies, with company tags and answer links. |
| [bmadone/senior-software-engineer](https://github.com/bmadone/senior-software-engineer) | Topic list for senior engineering (architecture, CI/CD, security, estimation, and so on). This repo has links, not questions, so topic 15 contains new questions and answers written for this bank. |

## Contents

Each file in [topics/](topics/) groups questions by theme. Every question shows where it came from (`Source:`) and, for the company-wise source, the companies it is `Asked at`.

| # | Topic | Questions |
| --- | --- | --- |
| 01 | [LLM fundamentals and architecture](topics/01-llm-fundamentals-and-architecture.md) | 109 |
| 02 | [Inference, serving and cost](topics/02-inference-serving-and-cost.md) | 70 |
| 03 | [Prompting and context engineering](topics/03-prompting-and-context-engineering.md) | 15 |
| 04 | [RAG and retrieval](topics/04-rag-and-retrieval.md) | 52 |
| 05 | [Agents and tool use](topics/05-agents-and-tool-use.md) | 54 |
| 06 | [Fine-tuning, post-training and alignment](topics/06-fine-tuning-and-alignment.md) | 43 |
| 07 | [Evaluation and observability](topics/07-evaluation-and-observability.md) | 63 |
| 08 | [Safety, security and responsible AI](topics/08-safety-security-and-responsible-ai.md) | 46 |
| 09 | [Multimodal, speech and voice](topics/09-multimodal-speech-and-voice.md) | 25 |
| 10 | [AI system design](topics/10-ai-system-design.md) | 93 |
| 11 | [Coding and data structures](topics/11-coding-and-data-structures.md) | 97 |
| 12 | [Applied scenarios and business judgment](topics/12-applied-and-business-judgment.md) | 34 |
| 13 | [Reasoning models](topics/13-reasoning-models.md) | 8 |
| 14 | [Behavioral and culture](topics/14-behavioral-and-culture.md) | 34 |
| 15 | [Senior engineering gap-fill](topics/15-senior-engineering-gap-fill.md) | 42 (answers included) |

Totals: about 785 questions after de-duplication, including the 42 gap-fill entries.

## Diagrams

The [images/](images/) folder has SVG diagrams for the core concepts: decoder transformer block, KV cache, LLM serving stack, RAG pipeline, agent loop, evaluation loop, and a generic LLM system-design template.

## How to use

1. Read one question and answer it aloud in under two minutes.
2. Open the source link to compare with the full answer.
3. For company prep, filter the `Asked at` tags for the target company.
4. Topic 15 has written answers. For the other topics, write your own answer first and then check the source.

## Notes

- The answers for topics 01 to 14 are not reproduced here. The sources hold them, and the bank links to them so the original authors' text stays with them.
- Company tags come from community reports. They show where a question was reported, not what the company asks now.
- Check the source repos for updates; they change often.
