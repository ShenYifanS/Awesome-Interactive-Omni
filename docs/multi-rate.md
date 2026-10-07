# 🔄 Multi-rate interactive intelligence

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**How can fast interaction and slow reasoning stay consistent?**

Multi-rate intelligence coordinates computations with different deadlines and commitment levels. A fast interaction process can acknowledge or yield while slower reasoning, retrieval or memory proceeds. The difficult boundary is deciding whether a returning result still belongs in the conversation.

Survey sections: **8, 9.1**.

## An interface for fast and slow computation

| Coordination decision | What must be known |
| --- | --- |
| Delegate | The current intent, sufficient evidence and the task's latency/commitment requirements. |
| Package context | Which sources, observations and user constraints the background task is allowed to use. |
| Validate a return | Whether the result's request version still agrees with live intent and available evidence. |
| Insert or defer | Whether the result adds useful information at the current conversational moment. |
| Cancel or revise | Which work and queued output are obsolete, and what effects have already occurred. |
| Consolidate | What was heard or acted upon and should remain in persistent state. |

## Two different trade-offs

**Adaptation:** does adding speech and interaction preserve the backbone's capabilities? Evaluate the underlying model before and after adaptation with controlled content tasks.

**Execution:** can preserved intelligence be used before a decision or spoken commitment is required? Report informative-answer delay, correction handling and stale-result use together with response onset.

### Concurrent thinking and speaking

Language reasoning can be interleaved with speech or maintained as latent computation during perception.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexSLA: A full-duplex spoken language model with synchronized speech, language, and action](https://arxiv.org/abs/2605.20755) | arXiv 2026 | [Code](https://github.com/hyzhang24/DuplexSLA) · [Ref 338](bibliography.md#ref-338) |
| [SHANKS: Simultaneous hearing and thinking for spoken language models](https://aclanthology.org/2026.acl-long.404/) | ACL 2026 | [Project](https://d223302.github.io/SHANKS/) · [Ref 44](bibliography.md#ref-044) |
| [STITCH: Simultaneous thinking and talking with chunked reasoning for spoken language models](https://openreview.net/forum?id=5Z1eMhCeTb) | ICLR 2026 | [Code](https://github.com/d223302/STITCH) · [Ref 45](bibliography.md#ref-045) |
| [The silent thought: Modeling internal cognition in full-duplex spoken dialogue models via latent reasoning](https://arxiv.org/abs/2603.17837) | ICML 2026 | [Ref 291](bibliography.md#ref-291) |
| [Thinking-while-speaking: A controlled, interleaved reasoning method for real-time speech generation](https://arxiv.org/abs/2605.20946) | arXiv 2026 | [Ref 65](bibliography.md#ref-065) |
| [Video streaming thinking: Videollms can watch and think simultaneously](https://arxiv.org/abs/2603.12262) | ECCV 2026 | [Code](https://github.com/1ranGuan/VST) · [Ref 99](bibliography.md#ref-099) |
| [Can speech LLMs think while listening?](https://arxiv.org/abs/2510.07497) | arXiv 2025 | [Ref 243](bibliography.md#ref-243) |

### Asynchronous retrieval, tools and memory

Track delegation, result arrival and the version of the request that produced a result.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexOmni: Real-time listening, seeing, thinking, and speaking for full-duplex interaction](https://arxiv.org/abs/2606.09186) | arXiv 2026 | [Code](https://github.com/MuyeHuang/DuplexOmni) · [Ref 114](bibliography.md#ref-114) |
| [Interaction models: A scalable approach to human-ai collaboration](https://thinkingmachines.ai/blog/interaction-models/) | 2026 | [Ref 262](bibliography.md#ref-262) |
| [MoshiRAG: Asynchronous knowledge retrieval for full-duplex speech language models](https://icml.cc/virtual/2026/poster/66336) | ICML 2026 | [Code](https://github.com/kyutai-labs/moshi-rag) · [Ref 46](bibliography.md#ref-046) |
| [Speculative interaction agents: Building real-time agents with asynchronous I/O and speculative tool calling](https://arxiv.org/abs/2605.13360) | arXiv 2026 | [Ref 105](bibliography.md#ref-105) |
| [Stream rag: Instant and accurate spoken dialogue systems with streaming tool usage](https://arxiv.org/abs/2510.02044) | ICML 2026 | [Ref 11](bibliography.md#ref-011) |
| [StreamArena: Toward continuous, interactive, and long-horizon agentic streaming video understanding](https://arxiv.org/abs/2608.05703) | arXiv 2026 | [Code](https://github.com/JIA-Lab-research/StreamArena) · [Ref 341](bibliography.md#ref-341) |
| [When does streaming tool use help? characterizing tool-intent stabilization in streaming retrieval-augmented generation](https://arxiv.org/abs/2606.20113) | arXiv 2026 | [Code](https://github.com/elroy-galbraith/stablize_CRAG) · [Ref 86](bibliography.md#ref-086) |
| [AsyncVoice agent: Real-time explanation for LLM planning and reasoning](https://arxiv.org/abs/2510.16156) | ASRU 2025 | [Ref 168](bibliography.md#ref-168) |
| [EgoMem: Lifelong memory agent for full-duplex omnimodal models](https://arxiv.org/abs/2509.11914) | arXiv 2025 | [Ref 313](bibliography.md#ref-313) |

### Preserving capability during adaptation

Freezing, specialized streams and modality-aware parameters are responses to capability interference; compare under controlled conditions.

| Paper | Venue | Resources |
| --- | --- | --- |
| [BayLing-Duplex: Native full-duplex speech dialogue with a single autoregressive LLM](https://arxiv.org/abs/2606.14528) | arXiv 2026 | [Code](https://github.com/BayLing-Models/BayLing-Duplex) · [Ref 74](bibliography.md#ref-074) |
| [Closing the gap between text and speech understanding in LLMs](https://openreview.net/forum?id=dDHnO3Vhyj) | ICLR 2026 | [Ref 53](bibliography.md#ref-053) |
| [JoyAI-Talker: Full-duplex speech interactive large model built for empathetic voice agents](https://arxiv.org/abs/2608.01119) | arXiv 2026 | [Ref 20](bibliography.md#ref-020) |
| [MoST: Mixing speech and text with modality-aware mixture of experts](https://arxiv.org/abs/2601.10272) | arXiv 2026 | [Code](https://github.com/NUS-HPC-AI-Lab/MoST) · [Ref 176](bibliography.md#ref-176) |
| [Multi-faceted interactivity alignment in full-duplex speech models](https://arxiv.org/abs/2606.11167) | EMNLP 2026 | [Model](https://huggingface.co/kyutai/personaplex-rl-seamless) · [Ref 202](bibliography.md#ref-202) |
| [Understanding textual capability degradation in speech LLMs via parameter importance analysis](https://doi.org/10.1109/ICASSP55912.2026.11461684) | ICASSP 2026 | [Ref 270](bibliography.md#ref-270) |
| [DeepOmni: Towards seamless and smart speech interaction with adaptive modality-specific MoE](https://arxiv.org/abs/2506.21864) | arXiv 2025 | [Code](https://github.com/talkking/DeepTalk) · [Ref 238](bibliography.md#ref-238) |
| [Freeze-Omni: A smart and low latency speech-to-speech dialogue model with frozen LLM](https://proceedings.mlr.press/v267/wang25aw.html) | ICML 2025 | [Code](https://github.com/VITA-MLLM/Freeze-Omni) · [Ref 281](bibliography.md#ref-281) |
| [Qwen3-Omni technical report](https://arxiv.org/abs/2509.17765) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen3-Omni) · [Ref 301](bibliography.md#ref-301) |
| [URO-Bench: Towards comprehensive evaluation for end-to-end spoken dialogue models](https://aclanthology.org/2025.findings-emnlp.933/) | EMNLP Findings 2025 | [Code](https://github.com/Ruiqi-Yan/URO-Bench) · [Ref 303](bibliography.md#ref-303) |

### Runtime coordination and resource budgets

Balance interaction deadlines with inference cost, bounded state and the opportunity to update or abandon speculative work.

| Paper | Venue | Resources |
| --- | --- | --- |
| [LiveServe: Interaction-aware serving for real-time omni-modal LLMs](https://arxiv.org/abs/2606.22983) | arXiv 2026 | [Ref 344](bibliography.md#ref-344) |
| [Taming Latency-Memory Trade-Off in MoE-Based LLM Serving via Fine-Grained Expert Offloading](https://doi.org/10.1145/3767295.3769319) | EuroSys 2026 | [Code](https://github.com/IntelliSys-Lab/FineMoE-EuroSys26) · [Ref 318](bibliography.md#ref-318) |
| [CE-CoLLM: Efficient and adaptive large language models through cloud-edge collaboration](https://ieeexplore.ieee.org/document/11169709/) | ICWS 2025 | [Ref 129](bibliography.md#ref-129) |
| [DistServe: Disaggregating prefill and decoding for goodput-optimized large language model serving](https://www.usenix.org/conference/osdi24/presentation/zhong-yinmin) | OSDI 2024 | [Code](https://github.com/LLMServe/DistServe) · [Ref 346](bibliography.md#ref-346) |
| [Efficient streaming language models with attention sinks](https://openreview.net/forum?id=NG7sS51zVF) | ICLR 2024 | [Code](https://github.com/mit-han-lab/streaming-llm) · [Ref 295](bibliography.md#ref-295) |
| [Taming throughput-latency tradeoff in LLM inference with Sarathi-Serve](https://www.usenix.org/conference/osdi24/presentation/agrawal) | OSDI 2024 | [Code](https://github.com/microsoft/sarathi-serve) · [Ref 4](bibliography.md#ref-004) |
| [Efficient memory management for large language model serving with PagedAttention](https://doi.org/10.1145/3600006.3613165) | SOSP 2023 | [Code](https://github.com/vllm-project/vllm) · [Ref 141](bibliography.md#ref-141) |
| [Speculative decoding with big little decoder](https://proceedings.neurips.cc/paper_files/paper/2023/hash/7b97adeafa1c51cf65263459ca9d0d7c-Abstract-Conference.html) | NeurIPS 2023 | [Code](https://github.com/kssteven418/BigLittleDecoder) · [Ref 136](bibliography.md#ref-136) |
