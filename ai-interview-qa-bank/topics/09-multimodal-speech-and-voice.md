# 09. Multimodal, speech and voice

25 questions. Sources are tagged per question. Full answers are in the linked source repo.

---

09.001  How do vision-language models get images into an LLM: projector, cross-attention, or native tokens?
> Asked at: Alibaba, Meta | Source: Company-wise (pallavi-shekhar)

09.002  What changes when you move from images to video?
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

09.003  Budget the latency for a real-time voice agent: VAD, ASR, LLM, TTS, network. Where does the time go?
> Asked at: ElevenLabs, Sarvam AI | Source: Company-wise (pallavi-shekhar)

09.004  Design barge-in / interruption handling for a voice agent.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.005  Cascaded ASR+LLM+TTS versus native speech-to-speech: argue both sides.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.006  How do you evaluate ASR quality beyond WER, and TTS quality when there is no single correct output?
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.007  How do you handle code-switching and accents in a production ASR system?
> Asked at: Abridge, Sarvam AI | Source: Company-wise (pallavi-shekhar)

09.008  Explain streaming TTS chunking and jitter-buffer sizing.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.009  Design a diarisation system and explain how you attribute roles, not just clusters.
> Asked at: Abridge | Source: Company-wise (pallavi-shekhar)

09.010  How would you build multimodal retrieval over images, video and text in one index?
> Asked at: Multimodal, Speech and Voice AI | Source: Company-wise (pallavi-shekhar)

09.011  How do modern multimodal models get image and video understanding into an LLM, and what changes for video specifically?
> Asked at: Meta | Source: Company-wise (pallavi-shekhar)

09.012  Qwen2.5-VL uses a native dynamic-resolution ViT with window attention and multimodal RoPE. Why native resolution instead of fixed tiling, and what does MRoPE encode?
> Asked at: Alibaba | Source: Company-wise (pallavi-shekhar)

09.013  Build a Voice Activity Detector from scratch. How do you make it robust for phone-quality Indian-language audio?
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

09.014  Whisper transcribes Hinglish poorly, often forcing output into one language or hallucinating. Why, and how would you build an ASR that handles code-mixed speech?
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

09.015  Bulbul-style TTS has to speak code-mixed, mixed-script text naturally. What are the hard parts of text normalization and prosody for Indian-language TTS?
> Asked at: Sarvam AI | Source: Company-wise (pallavi-shekhar)

09.016  How would you fuse camera, radar and IMU inputs into a single perception stack, and where would you fuse them?
> Asked at: Tesla | Source: Company-wise (pallavi-shekhar)

09.017  Your chat agent is moving to the phone. What actually changes?
> Asked at: Sierra | Source: Company-wise (pallavi-shekhar)

09.018  Budget the end-to-end latency for a real-time voice agent. Why is time-to-first-audio a different problem from an LLM's time-to-first-token?
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.019  Text normalisation is where TTS quality actually dies in production. Walk me through it.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.020  Design the dubbing pipeline: an English video becomes Spanish, same speakers, same timing.
> Asked at: ElevenLabs | Source: Company-wise (pallavi-shekhar)

09.021  Our audio is a clinic room: two or three speakers, background noise, accents, and a vocabulary full of drug names. How would you build and improve the ASR for that?
> Asked at: Abridge | Source: Company-wise (pallavi-shekhar)

09.022  What is a vision-language-action model, and how is it different from an LLM with tools?
> Asked at: Figure AI | Source: Company-wise (pallavi-shekhar)

09.023  Helix splits into a large slow model and a small fast one. Why not run a single end-to-end network?
> Asked at: Figure AI | Source: Company-wise (pallavi-shekhar)

09.024  Explain action chunking. Why predict a sequence of future actions instead of the next one?
> Asked at: Figure AI | Source: Company-wise (pallavi-shekhar)

09.025  Why carry lidar, radar and cameras rather than cameras alone? Where would you fuse them?
> Asked at: Waymo | Source: Company-wise (pallavi-shekhar)

