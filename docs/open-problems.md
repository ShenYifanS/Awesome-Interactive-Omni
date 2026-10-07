# 🔭 Open problems and research directions

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**Which combinations of capabilities are still missing?**

The agenda is about sustaining capabilities together: continuous perception, reasoning, timing, memory and repair within one interaction and resource budget.

Survey sections: **9**.

## Research questions and concrete evaluation targets

| Direction | Candidate evaluation target proposed by the survey |
| --- | --- |
| Joint content and timing | Quality–latency frontier, premature responses, accuracy after interruption. |
| Persistent state | Retrieval versus elapsed time, contradiction rate, task-state recovery and memory-normalized accuracy. |
| Tool cancellation and repair | Correction recovery, stale content, wasted calls and time to a revised action. |
| Multi-party interaction | Addressee accuracy, wrong-speaker responses and speaker-conditioned interruption behavior. |
| Multilingual interaction | Per-language timing and quality, code-switch repair and backchannel appropriateness. |
| Controllable policy | Adherence to listen/backchannel/interrupt/continue instructions and policy-switch latency. |
| Open-world robustness | Timely interventions, false alarms, privacy leakage and behavior under delayed media. |

### Joint intelligence–interactivity evaluation

Measure answer quality, temporal appropriateness and cost in the same episodes, including corrections and tool returns.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Audio MultiChallenge: A multi-turn evaluation of spoken dialogue systems on natural human interaction](https://aclanthology.org/2026.acl-long.1654/) | ACL 2026 | [Dataset](https://huggingface.co/datasets/ScaleAI/audiomc) · [Ref 96](bibliography.md#ref-096) |
| [Full-duplex-bench-v2: A multi-turn evaluation framework for duplex dialogue systems with an automated examiner](https://aclanthology.org/2026.acl-short.4/) | ACL 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 164](bibliography.md#ref-164) |
| [Full-duplex-bench-v3: Benchmarking tool use for full-duplex voice agents under real-world disfluency](https://doi.org/10.48550/arXiv.2604.04847) | arXiv 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 163](bibliography.md#ref-163) |
| [Instruct-FD: Can your full-duplex speech system follow turn-taking instructions?](https://arxiv.org/abs/2607.20460) | arXiv 2026 | [Ref 259](bibliography.md#ref-259) |
| [OmniInteract: Benchmarking real-world streaming interaction for real-time omnimodal assistants](https://arxiv.org/abs/2605.26485) | arXiv 2026 | [Code](https://github.com/Lucky-Lance/OmniInteract) · [Ref 177](bibliography.md#ref-177) |
| [Full-Duplex-Bench: A benchmark to evaluate full-duplex spoken dialogue models on turn-taking capabilities](https://doi.org/10.1109/ASRU65441.2025.11433838) | ASRU 2025 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 161](bibliography.md#ref-161) |
| [OmniMMI: A comprehensive multi-modal interaction benchmark in streaming video contexts](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_OmniMMI_A_Comprehensive_Multi-modal_Interaction_Benchmark_in_Streaming_Video_Contexts_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/OmniMMI/OmniMMI) · [Ref 284](bibliography.md#ref-284) |

### Persistent and proactive interaction

Maintain source-aware, revisable state across long audiovisual sessions while deciding when an intervention is useful.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Beyond retrieval: Progressive latent memory evolution for streaming video understanding](https://arxiv.org/abs/2609.04131) | arXiv 2026 | [Ref 220](bibliography.md#ref-220) |
| [Proact-VL: A proactive videollm for real-time AI companions](https://openreview.net/forum?id=k9PKgV0L4C) | ICML 2026 | [Code](https://github.com/microsoft/AnthropomorphicIntelligence/tree/main/Proact-VL) · [Ref 304](bibliography.md#ref-304) |
| [StreamArena: Toward continuous, interactive, and long-horizon agentic streaming video understanding](https://arxiv.org/abs/2608.05703) | arXiv 2026 | [Code](https://github.com/JIA-Lab-research/StreamArena) · [Ref 341](bibliography.md#ref-341) |
| [ContextAgent: Context-aware proactive LLM agents with open-world sensory perceptions](https://proceedings.neurips.cc/paper_files/paper/2025/hash/f4e5cd2079f5a6cf5176818add841531-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/openaiotlab/ContextAgent) · [Ref 305](bibliography.md#ref-305) |
| [EgoMem: Lifelong memory agent for full-duplex omnimodal models](https://arxiv.org/abs/2509.11914) | arXiv 2025 | [Ref 313](bibliography.md#ref-313) |
| [LongMemEval: Benchmarking chat assistants on long-term interactive memory](https://openreview.net/forum?id=pZiyCaVuti) | ICLR 2025 | [Code](https://github.com/xiaowu0162/LongMemEval) · [Ref 290](bibliography.md#ref-290) |

### Social, multilingual and controllable interaction

Move beyond dyadic default behavior toward addressee-aware, multilingual and instruction-conditioned floor control.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexGen: Adaptive synthesis of human-ai turn-taking dialogues](https://arxiv.org/abs/2607.26178) | EMNLP 2026 | [Code](https://github.com/duplexgen/duplexgen-code) · [Ref 137](bibliography.md#ref-137) |
| [Instruct-FD: Can your full-duplex speech system follow turn-taking instructions?](https://arxiv.org/abs/2607.20460) | arXiv 2026 | [Ref 259](bibliography.md#ref-259) |
| [M3-DuplexBench: A multi-turn, multilingual, multidomain benchmark for full-duplex spoken dialogue models](https://arxiv.org/abs/2607.29125) | arXiv 2026 | [Ref 85](bibliography.md#ref-085) |
| [MuVAP: Multimodal Multiparty Voice Activity Projection for Turn-taking Prediction in the Wild](https://arxiv.org/abs/2606.16731) | arXiv 2026 | [Code](https://github.com/Haotian-Qi/MuVAP) · [Ref 215](bibliography.md#ref-215) |
| [PersonaPlex: Voice and role control for full duplex conversational speech models](https://doi.org/10.1109/ICASSP55912.2026.11463413) | ICASSP 2026 | [Code](https://github.com/NVIDIA/personaplex) · [Ref 231](bibliography.md#ref-231) |
| [An LLM benchmark for addressee recognition in multi-modal multi-party dialogue](https://aclanthology.org/2025.iwsds-1.36/) | IWSDS 2025 | [Ref 118](bibliography.md#ref-118) |
| [Multilingual turn-taking prediction using voice activity projection](https://aclanthology.org/2024.lrec-main.1036/) | LREC-COLING 2024 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 116](bibliography.md#ref-116) |

### Safe and efficient open-world operation

Evaluate continuous privacy and safety decisions alongside robustness, latency and resource growth.

| Paper | Venue | Resources |
| --- | --- | --- |
| [IRAF: Interference-resilient adaptive fusion for noise-robust end-to-end full-duplex spoken dialogue systems](https://arxiv.org/abs/2606.06559) | arXiv 2026 | [Ref 345](bibliography.md#ref-345) |
| [LiveServe: Interaction-aware serving for real-time omni-modal LLMs](https://arxiv.org/abs/2606.22983) | arXiv 2026 | [Ref 344](bibliography.md#ref-344) |
| [PlayJev: A Multimodal JEV-Like Model for Small Games](https://github.com/OmniJev/PlayJev) | GitHub 2026 | [Ref 204](bibliography.md#ref-204) |
| [Privacy-preserving end-to-end full-duplex speech dialogue models](https://arxiv.org/abs/2603.08179) | arXiv 2026 | [Ref 140](bibliography.md#ref-140) |
| [Protecting bystander privacy via selective hearing in audio LLMs](https://aclanthology.org/2026.acl-long.693/) | ACL 2026 | [Code](https://github.com/Elocinacademia/SelectiveHearing-Bench) · [Ref 332](bibliography.md#ref-332) |
| [CE-CoLLM: Efficient and adaptive large language models through cloud-edge collaboration](https://ieeexplore.ieee.org/document/11169709/) | ICWS 2025 | [Ref 129](bibliography.md#ref-129) |
| [Omni-SafetyBench: A Benchmark for Safety Evaluation of Audio-Visual Large Language Models](https://arxiv.org/abs/2508.07173) | arXiv 2025 | [Code](https://github.com/THU-BPM/Omni-SafetyBench) · [Ref 207](bibliography.md#ref-207) |
