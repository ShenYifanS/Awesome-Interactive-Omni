# ⚡ Realizing omni interactivity

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**When should the system speak, wait, stop or revise?**

Interaction quality depends on response timing and control, together with the serving and playback stack. Streaming output alone does not demonstrate simultaneous listening, semantic repair or reliable cancellation.

Survey sections: **6**.

## Observe the whole interaction

| Event | What a system should reconcile |
| --- | --- |
| User pauses | Whether the user is hesitating, yielding or inviting a backchannel. |
| User overlaps speech | Whether this is an interruption, backchannel, side conversation or background speech. |
| User corrects the request | The current interpretation, queued output, pending work and retained state. |
| A tool returns | Whether its result belongs to the current request and can safely enter the response. |
| Playback is cut off | The difference between generated, buffered and actually heard content. |
| Session grows longer | Memory retention, latency drift, entity consistency and resource bounds. |

### Latency and responsiveness

Separate first-token, first-audio, informative-answer and interruption latency; report the hardware and event boundaries.

| Paper | Venue | Resources |
| --- | --- | --- |
| [LiveServe: Interaction-aware serving for real-time omni-modal LLMs](https://arxiv.org/abs/2606.22983) | arXiv 2026 | [Ref 344](bibliography.md#ref-344) |
| [Freeze-Omni: A smart and low latency speech-to-speech dialogue model with frozen LLM](https://proceedings.mlr.press/v267/wang25aw.html) | ICML 2025 | [Code](https://github.com/VITA-MLLM/Freeze-Omni) · [Ref 281](bibliography.md#ref-281) |
| [LLaMA-Omni: Seamless speech interaction with large language models](https://openreview.net/forum?id=PYmrUQmMEw) | ICLR 2025 | [Code](https://github.com/ictnlp/LLaMA-Omni) · [Ref 72](bibliography.md#ref-072) |
| [Moshi: a speech-text foundation model for real-time dialogue](https://doi.org/10.48550/arXiv.2410.00037) | arXiv 2024 | [Code](https://github.com/kyutai-labs/moshi) · [Ref 59](bibliography.md#ref-059) |
| [PSLM: Parallel generation of text and speech with LLMs for low-latency spoken dialogue systems](https://aclanthology.org/2024.findings-emnlp.151/) | EMNLP Findings 2024 | [Ref 190](bibliography.md#ref-190) |
| [Taming throughput-latency tradeoff in LLM inference with Sarathi-Serve](https://www.usenix.org/conference/osdi24/presentation/agrawal) | OSDI 2024 | [Code](https://github.com/microsoft/sarathi-serve) · [Ref 4](bibliography.md#ref-004) |
| [Sarathi: Efficient LLM inference by piggybacking decodes with chunked prefills](https://arxiv.org/abs/2308.16369) | arXiv 2023 | [Ref 3](bibliography.md#ref-003) |
| [Low-latency incremental text-to-speech synthesis with distilled context prediction network](https://doi.org/10.1109/ASRU51503.2021.9687904) | ASRU 2021 | [Project](https://takaaki-saeki.github.io/itts_distil_demo/) · [Ref 233](bibliography.md#ref-233) |
| [High quality streaming speech synthesis with low, sentence-length-independent latency](https://www.isca-archive.org/interspeech_2020/ellinas20_interspeech.html) | Interspeech 2020 | [Ref 70](bibliography.md#ref-070) |
| [Incremental text-to-speech synthesis with prefix-to-prefix framework](https://aclanthology.org/2020.findings-emnlp.346/) | EMNLP Findings 2020 | [Project](https://inctts.github.io/) · [Ref 179](bibliography.md#ref-179) |

### Turn-taking, silence and backchannels

Appropriate timing depends on conversational context and role. A lower delay is not always a better decision.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Instruct-FD: Can your full-duplex speech system follow turn-taking instructions?](https://arxiv.org/abs/2607.20460) | arXiv 2026 | [Ref 259](bibliography.md#ref-259) |
| [Synchronization and turn-taking in full-duplex speech dialogue models](https://arxiv.org/abs/2605.20356) | arXiv 2026 | [Ref 227](bibliography.md#ref-227) |
| [Yeah, un, oh: Continuous and real-time backchannel prediction with fine-tuning of voice activity projection](https://aclanthology.org/2025.naacl-long.367/) | NAACL 2025 | [Code](https://github.com/MaAI-Kyoto/MaAI) · [Ref 119](bibliography.md#ref-119) |
| [Real-time and continuous turn-taking prediction using voice activity projection](https://arxiv.org/abs/2401.04868) | IWSDS 2024 | [Code](https://github.com/inokoj/VAP-Realtime) · [Ref 117](bibliography.md#ref-117) |
| [Turn-taking and backchannel prediction with acoustic and large language model fusion](https://doi.org/10.1109/ICASSP48485.2024.10447196) | ICASSP 2024 | [Ref 276](bibliography.md#ref-276) |
| [What makes a good pause? investigating the turn-holding effects of fillers](https://www.internationalphoneticassociation.org/icphs-proceedings/ICPhS2023/full_papers/828.pdf) | ICPhS 2023 | [Code](https://github.com/ErikEkstedt/vap_fillers) · [Ref 126](bibliography.md#ref-126) |
| [Voice Activity Projection: Self-supervised Learning of Turn-taking Events](https://www.isca-archive.org/interspeech_2022/ekstedt22_interspeech.html) | Interspeech 2022 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 68](bibliography.md#ref-068) |
| [Turn-taking in conversational systems and human-robot interaction: A review](https://www.sciencedirect.com/science/article/pii/S088523082030111X) | Comput. Speech Lang. 2021 | [Ref 251](bibliography.md#ref-251) |
| [TurnGPT: a transformer-based language model for predicting turn-taking in spoken dialog](https://aclanthology.org/2020.findings-emnlp.268/) | EMNLP Findings 2020 | [Code](https://github.com/ErikEkstedt/TurnGPT) · [Ref 67](bibliography.md#ref-067) |
| [Towards a general, continuous model of turn-taking in spoken dialogue using LSTM recurrent neural networks](https://aclanthology.org/W17-5527/) | SIGDIAL 2017 | [Ref 250](bibliography.md#ref-250) |
| [Turn-taking in human communication: Origins and implications for language processing](https://doi.org/10.1016/j.tics.2015.10.010) | Trends Cogn. Sci. 2016 | [Ref 148](bibliography.md#ref-148) |
| [Timing in turn-taking and its implications for processing models of language](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2015.00731/full) | Front. Psychol. 2015 | [Ref 149](bibliography.md#ref-149) |
| [A simplest systematics for the organization of turn-taking for conversation](https://doi.org/10.2307/412243) | Language 1974 | [Ref 232](bibliography.md#ref-232) |

### Interruption, yielding and repair

Stopping playback is only one part of repair. Reconcile heard output, live intent, pending tools and remembered state.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Audio MultiChallenge: A multi-turn evaluation of spoken dialogue systems on natural human interaction](https://aclanthology.org/2026.acl-long.1654/) | ACL 2026 | [Dataset](https://huggingface.co/datasets/ScaleAI/audiomc) · [Ref 96](bibliography.md#ref-096) |
| [Full-duplex interaction in spoken dialogue systems: A comprehensive study from the icassp 2026 HumDial challenge](https://arxiv.org/abs/2604.21406) | arXiv 2026 | [Code](https://github.com/ASLP-lab/HumDial-FDBench) · [Ref 271](bibliography.md#ref-271) |
| [Full-Duplex-Bench v1.5: Evaluating overlap handling for full-duplex speech models](https://doi.org/10.1109/ICASSP55912.2026.11463576) | ICASSP 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 165](bibliography.md#ref-165) |
| [Full-duplex-bench-v2: A multi-turn evaluation framework for duplex dialogue systems with an automated examiner](https://aclanthology.org/2026.acl-short.4/) | ACL 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 164](bibliography.md#ref-164) |
| [IRAF: Interference-resilient adaptive fusion for noise-robust end-to-end full-duplex spoken dialogue systems](https://arxiv.org/abs/2606.06559) | arXiv 2026 | [Ref 345](bibliography.md#ref-345) |
| [Full-Duplex-Bench: A benchmark to evaluate full-duplex spoken dialogue models on turn-taking capabilities](https://doi.org/10.1109/ASRU65441.2025.11433838) | ASRU 2025 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 161](bibliography.md#ref-161) |
| [SALMONN-omni: A standalone speech LLM without codec injection for full-duplex conversation](https://proceedings.neurips.cc/paper_files/paper/2025/hash/233aee920dab065709145371b5900b8f-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/bytedance/SALMONN) · [Ref 324](bibliography.md#ref-324) |
| [SALMONN-omni: A codec-free LLM for full-duplex speech understanding and generation](https://arxiv.org/abs/2411.18138) | arXiv 2024 | [Code](https://github.com/bytedance/SALMONN) · [Ref 323](bibliography.md#ref-323) |

### Proactivity and adaptation

Initiate a response when the evidence and role warrant it, and adapt behavior to user corrections or interaction instructions.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexGen: Adaptive synthesis of human-ai turn-taking dialogues](https://arxiv.org/abs/2607.26178) | EMNLP 2026 | [Code](https://github.com/duplexgen/duplexgen-code) · [Ref 137](bibliography.md#ref-137) |
| [Instruct-FD: Can your full-duplex speech system follow turn-taking instructions?](https://arxiv.org/abs/2607.20460) | arXiv 2026 | [Ref 259](bibliography.md#ref-259) |
| [Proact-VL: A proactive videollm for real-time AI companions](https://openreview.net/forum?id=k9PKgV0L4C) | ICML 2026 | [Code](https://github.com/microsoft/AnthropomorphicIntelligence/tree/main/Proact-VL) · [Ref 304](bibliography.md#ref-304) |
| [ROMA: Real-time omni-multimodal assistant with interactive streaming understanding](https://aclanthology.org/2026.findings-acl.1153/) | ACL Findings 2026 | [Code](https://github.com/Eureka-Maggie/ROMA) · [Ref 263](bibliography.md#ref-263) |
| [User Preference Modeling for Conversational LLM Agents: Weak Rewards from Retrieval-Augmented Interaction](https://arxiv.org/abs/2603.20939) | arXiv 2026 | [Ref 101](bibliography.md#ref-101) |
| [ContextAgent: Context-aware proactive LLM agents with open-world sensory perceptions](https://proceedings.neurips.cc/paper_files/paper/2025/hash/f4e5cd2079f5a6cf5176818add841531-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/openaiotlab/ContextAgent) · [Ref 305](bibliography.md#ref-305) |
| [Dispider: Enabling video LLMs with active real-time interaction via disentangled perception, decision, and reaction](https://openaccess.thecvf.com/content/CVPR2025/html/Qian_Dispider_Enabling_Video_LLMs_with_Active_Real-Time_Interaction_via_Disentangled_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/Mark12Ding/Dispider) · [Ref 216](bibliography.md#ref-216) |
| [LiveStar: Live streaming assistant for real-world online video understanding](https://proceedings.neurips.cc/paper_files/paper/2025/hash/2ce4f0b8e24c45318352068603153590-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/sotayang/LiveStar) · [Ref 309](bibliography.md#ref-309) |
| [Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://doi.org/10.3233/FAIA251160) | ECAI 2025 | [Ref 43](bibliography.md#ref-043) |
| [OmniMMI: A comprehensive multi-modal interaction benchmark in streaming video contexts](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_OmniMMI_A_Comprehensive_Multi-modal_Interaction_Benchmark_in_Streaming_Video_Contexts_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/OmniMMI/OmniMMI) · [Ref 284](bibliography.md#ref-284) |
| [ProactiveVideoQA: A comprehensive benchmark evaluating proactive interactions in video large language models](https://doi.org/10.48550/arXiv.2507.09313) | arXiv 2025 | [Code](https://github.com/yellow-binary-tree/ProactiveVideoQA) · [Ref 282](bibliography.md#ref-282) |
| [StreamBridge: Turning your offline video large language model into a proactive streaming assistant](https://proceedings.neurips.cc/paper_files/paper/2025/hash/bf6939f9058a391c47014731b2486e2a-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/apple/ml-streambridge) · [Ref 274](bibliography.md#ref-274) |
| [Personalized Adaptation via In-Context Preference Learning](https://arxiv.org/abs/2410.14001) | arXiv 2024 | [Ref 145](bibliography.md#ref-145) |
| [Principles of Mixed-Initiative User Interfaces](https://doi.org/10.1145/302979.303030) | CHI 1999 | [Ref 106](bibliography.md#ref-106) |

### Serving, memory and client coordination

Scheduling, KV retention, asynchronous execution and playback acknowledgments protect conversational continuity.

| Paper | Venue | Resources |
| --- | --- | --- |
| [LiveServe: Interaction-aware serving for real-time omni-modal LLMs](https://arxiv.org/abs/2606.22983) | arXiv 2026 | [Ref 344](bibliography.md#ref-344) |
| [Speculative interaction agents: Building real-time agents with asynchronous I/O and speculative tool calling](https://arxiv.org/abs/2605.13360) | arXiv 2026 | [Ref 105](bibliography.md#ref-105) |
| [Taming Latency-Memory Trade-Off in MoE-Based LLM Serving via Fine-Grained Expert Offloading](https://doi.org/10.1145/3767295.3769319) | EuroSys 2026 | [Code](https://github.com/IntelliSys-Lab/FineMoE-EuroSys26) · [Ref 318](bibliography.md#ref-318) |
| [CE-CoLLM: Efficient and adaptive large language models through cloud-edge collaboration](https://ieeexplore.ieee.org/document/11169709/) | ICWS 2025 | [Ref 129](bibliography.md#ref-129) |
| [DistServe: Disaggregating prefill and decoding for goodput-optimized large language model serving](https://www.usenix.org/conference/osdi24/presentation/zhong-yinmin) | OSDI 2024 | [Code](https://github.com/LLMServe/DistServe) · [Ref 346](bibliography.md#ref-346) |
| [Efficient streaming language models with attention sinks](https://openreview.net/forum?id=NG7sS51zVF) | ICLR 2024 | [Code](https://github.com/mit-han-lab/streaming-llm) · [Ref 295](bibliography.md#ref-295) |
| [Leave no context behind: Efficient infinite context transformers with Infini-attention](https://arxiv.org/abs/2404.07143) | arXiv 2024 | [Ref 194](bibliography.md#ref-194) |
| [MInference 1.0: Accelerating pre-filling for long-context LLMs via dynamic sparse attention](https://proceedings.neurips.cc/paper_files/paper/2024/hash/5dfbe6f5671e82c76841ba687a8a9ecb-Abstract-Conference.html) | NeurIPS 2024 | [Code](https://github.com/microsoft/MInference) · [Ref 127](bibliography.md#ref-127) |
| [Splitwise: Efficient generative LLM inference using phase splitting](https://doi.org/10.1109/ISCA59077.2024.00019) | ISCA (arch) 2024 | [Code](https://github.com/Mutinifni/splitwise-sim) · [Ref 209](bibliography.md#ref-209) |
| [Efficient memory management for large language model serving with PagedAttention](https://doi.org/10.1145/3600006.3613165) | SOSP 2023 | [Code](https://github.com/vllm-project/vllm) · [Ref 141](bibliography.md#ref-141) |
| [H2O: Heavy-hitter oracle for efficient generative inference of large language models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/6ceefa7b15572587b78ecfcebb2827f8-Abstract.html) | NeurIPS 2023 | [Code](https://github.com/FMInference/H2O) · [Ref 343](bibliography.md#ref-343) |
| [Speculative decoding with big little decoder](https://proceedings.neurips.cc/paper_files/paper/2023/hash/7b97adeafa1c51cf65263459ca9d0d7c-Abstract-Conference.html) | NeurIPS 2023 | [Code](https://github.com/kssteven418/BigLittleDecoder) · [Ref 136](bibliography.md#ref-136) |
| [Orca: A distributed serving system for transformer-based generative models](https://www.usenix.org/conference/osdi22/presentation/yu) | OSDI 2022 | [Ref 317](bibliography.md#ref-317) |
| [ICASSP 2021 Acoustic Echo Cancellation Challenge: Datasets, Testing Framework, and Results](https://doi.org/10.1109/ICASSP39728.2021.9413457) | ICASSP 2021 | [Ref 254](bibliography.md#ref-254) |
| [Convolutional Neural Networks for Small-Footprint Keyword Spotting](https://doi.org/10.21437/Interspeech.2015-352) | Interspeech 2015 | [Ref 234](bibliography.md#ref-234) |
