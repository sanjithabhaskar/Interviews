# 06. Fine-tuning, post-training and alignment

43 questions. Sources are tagged per question. Full answers are in the linked source repo.

---

06.001  Walk me through RLHF end to end: reward model, policy optimisation, KL penalty.
> Asked at: Fine-Tuning, Post-Training and Alignment | Source: Company-wise (pallavi-shekhar)

06.002  What is DPO and why did it displace PPO-based RLHF at many labs? When is online RL still better?
> Asked at: Hugging Face, Scale AI | Source: Company-wise (pallavi-shekhar)

06.003  Explain GRPO and why dropping the value network matters at scale.
> Asked at: DeepSeek | Source: Company-wise (pallavi-shekhar)

06.004  Explain the LoRA decomposition mathematically. Why does it work, and how do you choose the rank r?
> Asked at: Fine-Tuning, Post-Training and Alignment | Source: Company-wise (pallavi-shekhar)

06.005  How does QLoRA achieve its memory reduction, and what are the quantization trade-offs?
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

06.006  Compare LoRA, prefix tuning, prompt tuning and full fine-tuning. When would you choose each?
> Asked at: Apple, Sarvam AI | Source: Company-wise (pallavi-shekhar)

06.007  What is catastrophic forgetting and how do you mitigate it during fine-tuning?
> Asked at: Mistral AI | Source: Company-wise (pallavi-shekhar)

06.008  Prompting, RAG or fine-tuning: give me your decision framework with cost and latency attached.
> Asked at: Cohere, Databricks, Glean, Microsoft, Mistral AI, OpenAI | Source: Company-wise (pallavi-shekhar)

06.009  Do the GPU memory maths for full fine-tuning a 7B model in bf16 with Adam. Now with LoRA.
> Asked at: Hugging Face, Mistral AI | Source: Company-wise (pallavi-shekhar)

06.010  What is RLVR (RL with verifiable rewards) and where does it beat a learned reward model?
> Asked at: Alibaba, Sarvam AI, Scale AI, Zhipu AI | Source: Company-wise (pallavi-shekhar)

06.011  Explain reward hacking in RLHF and how labs address it.
> Asked at: Scale AI | Source: Company-wise (pallavi-shekhar)

06.012  What is distillation, and how do you build a strong small model from a large one?
> Asked at: Alibaba | Source: Company-wise (pallavi-shekhar)

06.013  Explain Constitutional AI. What does it buy you over vanilla RLHF, and what doesn't it solve?
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

06.014  How do scaling laws influence the safety evaluation of large models?
> Asked at: Anthropic | Source: Company-wise (pallavi-shekhar)

06.015  Your pretraining loss suddenly diverges at step 300k of a long run. Diagnose and fix it.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

06.016  Design the training setup for a model that doesn't fit on one accelerator, say 70B parameters on a pod.
> Asked at: Google DeepMind and Google AI | Source: Company-wise (pallavi-shekhar)

06.017  Walk me through a post-training recipe to turn a pretrained base model into a personalised assistant.
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

06.018  You're training on tens of thousands of GPUs and hardware fails constantly. How do you keep goodput high?
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

06.019  Loss spikes mid-run on a large pretraining job. Walk me through your debugging process.
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

06.020  Design a deduplication pipeline for a web-scale pretraining corpus. It has to run as a streaming process.
> Asked at: xAI | Source: Company-wise (pallavi-shekhar)

06.021  After fine-tuning on a customer's task, target accuracy is up but the model got worse at everything else. What happened and what do you do?
> Asked at: Mistral AI | Source: Company-wise (pallavi-shekhar)

06.022  R1-Zero was trained with RL and essentially no SFT first. What did that show, and why did full R1 add SFT back?
> Asked at: DeepSeek | Source: Company-wise (pallavi-shekhar)

06.023  FP8 training at 671B scale is hard. What actually breaks in low precision, and how do you make it stable?
> Asked at: DeepSeek | Source: Company-wise (pallavi-shekhar)

06.024  How do you build a training dataset without triggering model collapse when much of your data is synthetic?
> Asked at: DeepSeek | Source: Company-wise (pallavi-shekhar)

06.025  DualPipe overlaps computation and communication in training. Why is that overlap the whole game at this scale, and what is the trade-off?
> Asked at: DeepSeek | Source: Company-wise (pallavi-shekhar)

06.026  Training a trillion-parameter model, attention logits can blow up and destabilise the run. What is going on, and how does something like MuonClip address it?
> Asked at: Moonshot AI | Source: Company-wise (pallavi-shekhar)

06.027  Kimi K1.5 scaled RL for reasoning without a process reward model or tree search. Why deliberately keep the RL recipe that simple?
> Asked at: Moonshot AI | Source: Company-wise (pallavi-shekhar)

06.028  GLM-4.5 is a hybrid reasoning model with a thinking mode and a direct-response mode. How do you build one model that does both, and what are the training and serving implications?
> Asked at: Zhipu AI | Source: Company-wise (pallavi-shekhar)

06.029  Why does long-horizon agentic RL need a disaggregated, asynchronous design (as in the slime framework) rather than colocated-synchronous?
> Asked at: Zhipu AI | Source: Company-wise (pallavi-shekhar)

06.030  GLM-4.5's post-training trains expert models per domain then unifies with self-distillation. Walk through why you would train specialists and then merge them.
> Asked at: Zhipu AI | Source: Company-wise (pallavi-shekhar)

06.031  Qwen3 uses strong-to-weak distillation, bootstrapping smaller models from flagship ones. How does that work and why is it cheaper?
> Asked at: Alibaba | Source: Company-wise (pallavi-shekhar)

06.032  Qwen's reasoning models train with RL using verifiable rewards on maths and code. Why is that preferred over PPO with a learned reward model for these domains?
> Asked at: Alibaba | Source: Company-wise (pallavi-shekhar)

06.033  Sarvam-M ships hybrid think/non-think modes and was post-trained with SFT then RLVR. How would you build that, and why RLVR over vanilla RLHF?
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

06.034  A regional government wants an assistant in a low-resource language with only a few thousand sentences of clean text. How do you adapt a model to it?
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

06.035  You have one on-device base model but a dozen features: summarization, rewriting, reply suggestions, tone adjustment. How do you specialise without shipping a dozen models?
> Asked at: Apple | Source: Company-wise (pallavi-shekhar)

06.036  How would you improve an on-device model using signals from user devices without collecting user content?
> Asked at: Apple | Source: Company-wise (pallavi-shekhar)

06.037  When would you fine-tune instead of using RAG or prompt engineering, and if you do, LoRA or full fine-tuning?
> Asked at: Databricks | Source: Company-wise (pallavi-shekhar)

06.038  A customer's distributed training job on your GPU cluster gets 55% scaling efficiency at 64 nodes. Debug it.
> Asked at: Together AI | Source: Company-wise (pallavi-shekhar)

06.039  Fine-tune an 8B model on a single 24 GB GPU. Walk me through the memory maths and the exact stack you'd use.
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

06.040  You're building a web-scale pretraining corpus (FineWeb-style). Walk me through the pipeline and how you decide whether each filter earns its place.
> Asked at: Hugging Face | Source: Company-wise (pallavi-shekhar)

06.041  Compare SFT, RLHF, DPO and RLVR for improving an instruction-tuned model. What data does each need, and when would you pick which?
> Asked at: Scale AI | Source: Company-wise (pallavi-shekhar)

06.042  We sell RL environments. Design one for “book a multi-city trip in a web travel app”, specify the reward, and tell me how you stop the policy hacking it.
> Asked at: Scale AI | Source: Company-wise (pallavi-shekhar)

06.043  You are training an agent model with end-to-end RL in your own harness. Walk through the environment and reward design.
> Asked at: Cognition | Source: Company-wise (pallavi-shekhar)

