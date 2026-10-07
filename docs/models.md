# 🧩 Models and architectures

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**Where does interaction control live?**

Compare systems by the state that receives new evidence and controls ongoing output. Adapted and model-native systems are two development paths; foreground–background coordination can be added across both.

Survey sections: **2, 4.1**.

## How to compare an architecture

| Record | Useful distinction |
| --- | --- |
| Input and output | Which modalities are accepted and emitted, and whether they are causal streams or completed segments. |
| Temporal state | Whether time, silence, overlap and speaker identity are represented explicitly. |
| Control location | Model prediction, external controller, runtime policy, or a combination. |
| Revision | Whether new input can update generation, stop playback and repair semantic state. |
| Reasoning path | Shared backbone, separate linguistic stream, specialized Talker, or asynchronous background computation. |
| Evidence | Paper claims, evaluated tasks, code, weights and data should be recorded separately. |

### Omni input and output models

Broad modality support and streaming generation must be distinguished from the ability to update an active response.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Ex-Omni-2D: Expressive omni-modal dialogue models with native visual presence](https://arxiv.org/abs/2608.10720) | arXiv 2026 | [Code](https://github.com/LOGO-CUHKSZ/Ex-Omni-2D-Code) · [Ref 339](bibliography.md#ref-339) |
| [MiniCPM-o 4.5: Towards real-time full-duplex omni-modal interaction](https://arxiv.org/abs/2604.27393) | arXiv 2026 | [Code](https://github.com/OpenBMB/MiniCPM-o) · [Ref 54](bibliography.md#ref-054) |
| [MiniMind-o technical report: An open small-scale speech-native omni model](https://arxiv.org/abs/2605.03937) | arXiv 2026 | [Code](https://github.com/jingyaogong/minimind-o) · [Ref 94](bibliography.md#ref-094) |
| [Qwen3.5-Omni technical report](https://arxiv.org/abs/2604.15804) | arXiv 2026 | [Ref 221](bibliography.md#ref-221) |
| [ROMA: Real-time omni-multimodal assistant with interactive streaming understanding](https://aclanthology.org/2026.findings-acl.1153/) | ACL Findings 2026 | [Code](https://github.com/Eureka-Maggie/ROMA) · [Ref 263](bibliography.md#ref-263) |
| [InteractiveOmni: A unified omni-modal model for audio-visual multi-turn dialogue](https://arxiv.org/abs/2510.13747) | arXiv 2025 | [Code](https://github.com/SenseTime-FVG/InteractiveOmni) · [Ref 264](bibliography.md#ref-264) |
| [LLaMA-Omni 2: LLM-Based Real-Time Spoken Chatbot with Autoregressive Streaming Speech Synthesis](https://aclanthology.org/2025.acl-long.912/) | ACL 2025 | [Code](https://github.com/ictnlp/LLaMA-Omni2) · [Ref 73](bibliography.md#ref-073) |
| [LLaMA-Omni: Seamless speech interaction with large language models](https://openreview.net/forum?id=PYmrUQmMEw) | ICLR 2025 | [Code](https://github.com/ictnlp/LLaMA-Omni) · [Ref 72](bibliography.md#ref-072) |
| [Qwen2.5-Omni technical report](https://arxiv.org/abs/2503.20215) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen2.5-Omni) · [Ref 300](bibliography.md#ref-300) |
| [Qwen3-Omni technical report](https://arxiv.org/abs/2509.17765) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen3-Omni) · [Ref 301](bibliography.md#ref-301) |
| [Vita-1.5: Towards GPT-4o level real-time vision and speech interaction](https://proceedings.neurips.cc/paper_files/paper/2025/hash/6ce9d51dded7dac82b3b4d3dbb1d73bc-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/VITA-MLLM/VITA) · [Ref 84](bibliography.md#ref-084) |
| [AnyGPT: Unified multimodal LLM with discrete sequence modeling](https://aclanthology.org/2024.acl-long.521/) | ACL 2024 | [Code](https://github.com/OpenMOSS/AnyGPT) · [Ref 331](bibliography.md#ref-331) |
| [Mini-Omni2: Towards open-source GPT-4o with vision, speech and duplex capabilities](https://arxiv.org/abs/2410.11190) | arXiv 2024 | [Code](https://github.com/gpt-omni/mini-omni2) · [Ref 298](bibliography.md#ref-298) |
| [Mini-Omni: Language models can hear, talk while thinking in streaming](https://arxiv.org/abs/2408.16725) | arXiv 2024 | [Code](https://github.com/gpt-omni/mini-omni) · [Ref 297](bibliography.md#ref-297) |
| [VITA: Towards open-source interactive omni multimodal LLM](https://arxiv.org/abs/2408.05211) | arXiv 2024 | [Code](https://github.com/VITA-MLLM/VITA) · [Ref 83](bibliography.md#ref-083) |

### Speech-native full-duplex models

Paired or synchronized streams expose silence, overlap and speaking/listening decisions to the model.

| Paper | Venue | Resources |
| --- | --- | --- |
| [BayLing-Duplex: Native full-duplex speech dialogue with a single autoregressive LLM](https://arxiv.org/abs/2606.14528) | arXiv 2026 | [Code](https://github.com/BayLing-Models/BayLing-Duplex) · [Ref 74](bibliography.md#ref-074) |
| [DuplexSLA: A full-duplex spoken language model with synchronized speech, language, and action](https://arxiv.org/abs/2605.20755) | arXiv 2026 | [Code](https://github.com/hyzhang24/DuplexSLA) · [Ref 338](bibliography.md#ref-338) |
| [JoyAI-Talker: Full-duplex speech interactive large model built for empathetic voice agents](https://arxiv.org/abs/2608.01119) | arXiv 2026 | [Ref 20](bibliography.md#ref-020) |
| [PersonaPlex: Voice and role control for full duplex conversational speech models](https://doi.org/10.1109/ICASSP55912.2026.11463413) | ICASSP 2026 | [Code](https://github.com/NVIDIA/personaplex) · [Ref 231](bibliography.md#ref-231) |
| [TurnGuide: Enhancing meaningful full duplex spoken interactions via dynamic turn-level text-speech interleaving](https://arxiv.org/abs/2508.07375) | Interspeech 2026 | [Code](https://github.com/dreamtheater123/TurnGuide) · [Ref 56](bibliography.md#ref-056) |
| [Language model can listen while speaking](https://ojs.aaai.org/index.php/AAAI/article/view/34665) | AAAI 2025 | [Project](https://ddlbojack.github.io/LSLM) · [Ref 181](bibliography.md#ref-181) |
| [NTPP: Generative speech language modeling for dual-channel spoken dialogue via next-token-pair prediction](https://proceedings.mlr.press/v267/wang25by.html) | ICML 2025 | [Code](https://github.com/Chaos96/NTPP) · [Ref 279](bibliography.md#ref-279) |
| [SALMONN-omni: A standalone speech LLM without codec injection for full-duplex conversation](https://proceedings.neurips.cc/paper_files/paper/2025/hash/233aee920dab065709145371b5900b8f-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/bytedance/SALMONN) · [Ref 324](bibliography.md#ref-324) |
| [Beyond turn-based interfaces: Synchronous LLMs as full-duplex dialogue agents](https://aclanthology.org/2024.emnlp-main.1192/) | EMNLP 2024 | [Project](https://syncllm.cs.washington.edu/) · [Ref 268](bibliography.md#ref-268) |
| [Moshi: a speech-text foundation model for real-time dialogue](https://doi.org/10.48550/arXiv.2410.00037) | arXiv 2024 | [Code](https://github.com/kyutai-labs/moshi) · [Ref 59](bibliography.md#ref-059) |
| [SALMONN-omni: A codec-free LLM for full-duplex speech understanding and generation](https://arxiv.org/abs/2411.18138) | arXiv 2024 | [Code](https://github.com/bytedance/SALMONN) · [Ref 323](bibliography.md#ref-323) |
| [Generative spoken dialogue language modeling](https://aclanthology.org/2023.tacl-1.15/) | TACL 2023 | [Code](https://github.com/facebookresearch/fairseq/tree/main/examples/textless_nlp/dgslm) · [Ref 199](bibliography.md#ref-199) |

### Cascaded and adapted systems

Streaming recognition, language reasoning and synthesis may be separately trained, with timing managed by orchestration.

| Paper | Venue | Resources |
| --- | --- | --- |
| [CrossOracle: An agentic framework for real-time expert personas with parallelized acoustic synthesis](https://aclanthology.org/2026.sigdial-1.18/) | SIGDIAL 2026 | [Ref 247](bibliography.md#ref-247) |
| [UAF: A unified audio front-end LLM for full-duplex speech interaction](https://arxiv.org/abs/2604.19221) | arXiv 2026 | [Ref 155](bibliography.md#ref-155) |
| [ChipChat: Low-latency cascaded conversational agent in MLX](https://machinelearning.apple.com/research/chipchat) | ASRU 2025 | [Ref 160](bibliography.md#ref-160) |
| [Freeze-Omni: A smart and low latency speech-to-speech dialogue model with frozen LLM](https://proceedings.mlr.press/v267/wang25aw.html) | ICML 2025 | [Code](https://github.com/VITA-MLLM/Freeze-Omni) · [Ref 281](bibliography.md#ref-281) |
| [Robust speech recognition via large-scale weak supervision](https://proceedings.mlr.press/v202/radford23a.html) | ICML 2023 | [Code](https://github.com/openai/whisper) · [Ref 223](bibliography.md#ref-223) |
| [Low-latency incremental text-to-speech synthesis with distilled context prediction network](https://doi.org/10.1109/ASRU51503.2021.9687904) | ASRU 2021 | [Project](https://takaaki-saeki.github.io/itts_distil_demo/) · [Ref 233](bibliography.md#ref-233) |
| [Incremental text-to-speech synthesis with prefix-to-prefix framework](https://aclanthology.org/2020.findings-emnlp.346/) | EMNLP Findings 2020 | [Project](https://inctts.github.io/) · [Ref 179](bibliography.md#ref-179) |
| [Sequence transduction with recurrent neural networks](https://arxiv.org/abs/1211.3711) | ICML Workshop 2012 | [Ref 98](bibliography.md#ref-098) |

### Foreground–background designs

Low-latency interaction can run alongside retrieval, reasoning, memory or tools. The same pattern may appear within one backbone or across multiple models.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexOmni: Real-time listening, seeing, thinking, and speaking for full-duplex interaction](https://arxiv.org/abs/2606.09186) | arXiv 2026 | [Code](https://github.com/MuyeHuang/DuplexOmni) · [Ref 114](bibliography.md#ref-114) |
| [Interaction models: A scalable approach to human-ai collaboration](https://thinkingmachines.ai/blog/interaction-models/) | 2026 | [Ref 262](bibliography.md#ref-262) |
| [MoshiRAG: Asynchronous knowledge retrieval for full-duplex speech language models](https://icml.cc/virtual/2026/poster/66336) | ICML 2026 | [Code](https://github.com/kyutai-labs/moshi-rag) · [Ref 46](bibliography.md#ref-046) |
| [STITCH: Simultaneous thinking and talking with chunked reasoning for spoken language models](https://openreview.net/forum?id=5Z1eMhCeTb) | ICLR 2026 | [Code](https://github.com/d223302/STITCH) · [Ref 45](bibliography.md#ref-045) |
| [Stream rag: Instant and accurate spoken dialogue systems with streaming tool usage](https://arxiv.org/abs/2510.02044) | ICML 2026 | [Ref 11](bibliography.md#ref-011) |
| [StreamArena: Toward continuous, interactive, and long-horizon agentic streaming video understanding](https://arxiv.org/abs/2608.05703) | arXiv 2026 | [Code](https://github.com/JIA-Lab-research/StreamArena) · [Ref 341](bibliography.md#ref-341) |
| [EgoMem: Lifelong memory agent for full-duplex omnimodal models](https://arxiv.org/abs/2509.11914) | arXiv 2025 | [Ref 313](bibliography.md#ref-313) |

### Fusion and specialization

Compare encoders, token interfaces, early fusion and expert routing without assuming any one choice guarantees native interaction.

| Paper | Venue | Resources |
| --- | --- | --- |
| [CogniRoute: Learning to route social evidence in omni-modal models](https://arxiv.org/abs/2606.20970) | arXiv 2026 | [Ref 240](bibliography.md#ref-240) |
| [JAVISDiT++: Unified modeling and optimization for joint audio-video generation](https://arxiv.org/abs/2602.19163) | ICLR 2026 | [Code](https://github.com/JavisVerse/JavisDiT) · [Ref 172](bibliography.md#ref-172) |
| [MoST: Mixing speech and text with modality-aware mixture of experts](https://arxiv.org/abs/2601.10272) | arXiv 2026 | [Code](https://github.com/NUS-HPC-AI-Lab/MoST) · [Ref 176](bibliography.md#ref-176) |
| [OmniEncoder: See, hear, and feel continuous motion like humans with one encoder](https://arxiv.org/abs/2605.01506) | arXiv 2026 | [Ref 17](bibliography.md#ref-017) |
| [DeepOmni: Towards seamless and smart speech interaction with adaptive modality-specific MoE](https://arxiv.org/abs/2506.21864) | arXiv 2025 | [Code](https://github.com/talkking/DeepTalk) · [Ref 238](bibliography.md#ref-238) |
| [Scaling laws for native multimodal models](https://openaccess.thecvf.com/content/ICCV2025/html/Shukor_Scaling_Laws_for_Native_Multimodal_Models_ICCV_2025_paper.html) | ICCV 2025 | [Code](https://github.com/apple/ml-l3m) · [Ref 244](bibliography.md#ref-244) |
| [Unveiling encoder-free vision-language models](https://proceedings.neurips.cc/paper_files/paper/2024/hash/5e2217482fa75556f1970be809acd3f8-Abstract-Conference.html) | NeurIPS 2024 | [Code](https://github.com/baaivision/EVE) · [Ref 62](bibliography.md#ref-062) |

### Commercial real-time systems

Official model pages, release announcements, and system cards.

| Paper | Venue | Resources |
| --- | --- | --- |
| [GPT-Realtime-2 model](https://developers.openai.com/api/docs/models/gpt-realtime-2) | 2026 | [Ref 206](bibliography.md#ref-206) |
| [Qwen3.5-Omni-Realtime: Real-time omni-modal interaction](https://docs.modelstudio.console.alibabacloud.com/en/model-studio/realtime) | 2026 | [Ref 6](bibliography.md#ref-006) |
| [SeedRealtime audio-visual full-duplex LLM released: Toward omni-modal natural interaction](https://seed.bytedance.com/en/blog/seedrealtime-audio-visual-full-duplex-llm-released-toward-omni-modal-natural-interaction) | 2026 | [Ref 24](bibliography.md#ref-024) |
| [Gemini live](https://gemini.google/overview/gemini-live/) | 2024 | [Ref 95](bibliography.md#ref-095) |
| [GPT-4o system card](https://arxiv.org/abs/2410.21276) | arXiv 2024 | [Ref 205](bibliography.md#ref-205) |
