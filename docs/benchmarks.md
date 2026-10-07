# 📊 Evaluation and benchmarks

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**Can a system be correct at the right moment?**

The survey uses six evaluation dimensions: latency, timing, content, robustness, long-session quality and repair. Public end-to-end suites, supporting prediction tasks and vendor-internal evaluations serve different purposes.

Survey sections: **7**.

## Six dimensions, different protocols

| Dimension | Question | Example measures or observations |
| --- | --- | --- |
| **Latency** | How quickly does useful interaction happen? | First token, first audible sample, time to informative answer, interruption response. |
| **Timing** | Was speaking or waiting appropriate? | Turn-transition behavior, premature takeover, backchannel timing. |
| **Content** | Was the response correct and instruction-consistent? | Task accuracy, instruction adherence, grounding, task success. |
| **Robustness** | Does behavior survive overlap and interference? | Behavior under background speech, noise, barge-in and side conversations. |
| **Long-session quality** | Does state remain coherent as the session grows? | Entity tracking, instruction retention, temporal retrieval, contradiction. |
| **Repair** | Does the system recover from a correction? | Corrected-intent success, stale-content rate, recovery after interruption. |

The survey proposes correction-recovery and stale-content measures as useful evaluation targets.

## Pick the right kind of evidence

| Resource type | Examples | What can be concluded |
| --- | --- | --- |
| End-to-end spoken interaction | FDB variants, HumDial-FDBench, M3-DuplexBench | Behavior under the suite's specific spoken protocol. |
| Online audiovisual interaction | OmniMMI, ProactiveVideoQA, StreamArena | Streaming understanding and response behavior as specified by the task. |
| Static or turn-bounded intelligence | OmniBench, Dynamic-SUPERB, VoiceBench | Content capability and relevant robustness controls, without automatically establishing full duplex. |
| Supporting primitives | TurnGPT, VAP, MuVAP, Charades-STA, RepCount | A component capability such as next-speaker prediction or temporal grounding. |
| Vendor-internal evaluation | TimeSpeak, CueSpeak, reported in [Interaction Models](bibliography.md#ref-225) | Vendor-reported evidence; exclude from public reproducibility rankings. |

**Important metric distinction:** the desired direction of Takeover Rate depends on the event. During a user's hesitation or backchannel opportunity, unwanted floor-taking is undesirable; when the user genuinely yields, an appropriate response is desirable. Never interpret “higher TOR” as uniformly better.

### Full-duplex spoken interaction

Probe floor-taking, overlap, multi-turn consistency, controllable behavior, and tool use under spoken disfluency.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Full-duplex interaction in spoken dialogue systems: A comprehensive study from the icassp 2026 HumDial challenge](https://arxiv.org/abs/2604.21406) | arXiv 2026 | [Code](https://github.com/ASLP-lab/HumDial-FDBench) · [Ref 271](bibliography.md#ref-271) |
| [Full-Duplex-Bench v1.5: Evaluating overlap handling for full-duplex speech models](https://doi.org/10.1109/ICASSP55912.2026.11463576) | ICASSP 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 165](bibliography.md#ref-165) |
| [Full-duplex-bench-v2: A multi-turn evaluation framework for duplex dialogue systems with an automated examiner](https://aclanthology.org/2026.acl-short.4/) | ACL 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 164](bibliography.md#ref-164) |
| [Full-duplex-bench-v3: Benchmarking tool use for full-duplex voice agents under real-world disfluency](https://doi.org/10.48550/arXiv.2604.04847) | arXiv 2026 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 163](bibliography.md#ref-163) |
| [Instruct-FD: Can your full-duplex speech system follow turn-taking instructions?](https://arxiv.org/abs/2607.20460) | arXiv 2026 | [Ref 259](bibliography.md#ref-259) |
| [M3-DuplexBench: A multi-turn, multilingual, multidomain benchmark for full-duplex spoken dialogue models](https://arxiv.org/abs/2607.29125) | arXiv 2026 | [Ref 85](bibliography.md#ref-085) |
| [Full-Duplex-Bench: A benchmark to evaluate full-duplex spoken dialogue models on turn-taking capabilities](https://doi.org/10.1109/ASRU65441.2025.11433838) | ASRU 2025 | [Code](https://github.com/DanielLin94144/Full-Duplex-Bench) · [Ref 161](bibliography.md#ref-161) |

### Streaming and proactive omni interaction

Measure causal audiovisual understanding and whether a system chooses an appropriate response time.

| Paper | Venue | Resources |
| --- | --- | --- |
| [OmniInteract: Benchmarking real-world streaming interaction for real-time omnimodal assistants](https://arxiv.org/abs/2605.26485) | arXiv 2026 | [Code](https://github.com/Lucky-Lance/OmniInteract) · [Ref 177](bibliography.md#ref-177) |
| [Proact-VL: A proactive videollm for real-time AI companions](https://openreview.net/forum?id=k9PKgV0L4C) | ICML 2026 | [Code](https://github.com/microsoft/AnthropomorphicIntelligence/tree/main/Proact-VL) · [Ref 304](bibliography.md#ref-304) |
| [StreamArena: Toward continuous, interactive, and long-horizon agentic streaming video understanding](https://arxiv.org/abs/2608.05703) | arXiv 2026 | [Code](https://github.com/JIA-Lab-research/StreamArena) · [Ref 341](bibliography.md#ref-341) |
| [StreamingBench: Assessing the gap for mllms to achieve streaming video understanding](https://doi.org/10.1109/ICASSP55912.2026.11463959) | ICASSP 2026 | [Code](https://github.com/THUNLP-MT/StreamingBench) · [Ref 166](bibliography.md#ref-166) |
| [OmniMMI: A comprehensive multi-modal interaction benchmark in streaming video contexts](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_OmniMMI_A_Comprehensive_Multi-modal_Interaction_Benchmark_in_Streaming_Video_Contexts_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/OmniMMI/OmniMMI) · [Ref 284](bibliography.md#ref-284) |
| [ProactiveVideoQA: A comprehensive benchmark evaluating proactive interactions in video large language models](https://doi.org/10.48550/arXiv.2507.09313) | arXiv 2025 | [Code](https://github.com/yellow-binary-tree/ProactiveVideoQA) · [Ref 282](bibliography.md#ref-282) |

### Spoken and multimodal intelligence

Use content-focused evaluations as capability controls; static accuracy does not establish full-duplex interaction.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Audio MultiChallenge: A multi-turn evaluation of spoken dialogue systems on natural human interaction](https://aclanthology.org/2026.acl-long.1654/) | ACL 2026 | [Dataset](https://huggingface.co/datasets/ScaleAI/audiomc) · [Ref 96](bibliography.md#ref-096) |
| [Evaluating cognitive age alignment in interactive AI agents](https://arxiv.org/abs/2605.17894) | arXiv 2026 | [Code](https://github.com/PediaMedAI/ChildAgentEval) · [Ref 242](bibliography.md#ref-242) |
| [From text to voice: A reproducible and verifiable framework for evaluating tool calling LLM agents](https://arxiv.org/abs/2605.15104) | arXiv 2026 | [Ref 144](bibliography.md#ref-144) |
| [VoiceBench: Benchmarking LLM-based voice assistants](https://aclanthology.org/2026.tacl-1.18/) | TACL 2026 | [Code](https://github.com/MatthewCYM/VoiceBench) · [Ref 41](bibliography.md#ref-041) |
| [Dynamic-SUPERB phase-2: A collaboratively expanding benchmark for measuring the capabilities of spoken language models with 180 tasks](https://openreview.net/forum?id=s7lzZpAW7T) | ICLR 2025 | [Code](https://github.com/dynamic-superb/dynamic-superb) · [Ref 113](bibliography.md#ref-113) |
| [MultiChallenge: A realistic multi-turn conversation evaluation benchmark challenging to frontier LLMs](https://aclanthology.org/2025.findings-acl.958/) | ACL Findings 2025 | [Code](https://github.com/ekwinox117/multi-challenge) · [Ref 60](bibliography.md#ref-060) |
| [OmniBench: Towards the future of universal omni-language models](https://proceedings.neurips.cc/paper_files/paper/2025/hash/2c7c4a12a9dcf7dace9896d08154c705-Abstract-Datasets_and_Benchmarks_Track.html) | NeurIPS 2025 | [Code](https://github.com/multimodal-art-projection/OmniBench) · [Ref 157](bibliography.md#ref-157) |
| [URO-Bench: Towards comprehensive evaluation for end-to-end spoken dialogue models](https://aclanthology.org/2025.findings-emnlp.933/) | EMNLP Findings 2025 | [Code](https://github.com/Ruiqi-Yan/URO-Bench) · [Ref 303](bibliography.md#ref-303) |
| [VoiceAgentBench: Are voice assistants ready for agentic tasks?](https://arxiv.org/abs/2510.07978) | arXiv 2025 | [Code](https://github.com/ola-krutrim/VoiceAgentBench) · [Ref 122](bibliography.md#ref-122) |
| [What is the visual cognition gap between humans and multimodal LLMs?](https://openreview.net/forum?id=78lTuD6wiO) | COLM 2025 | [Code](https://github.com/PediaMedAI/Cognition-MLLM) · [Ref 30](bibliography.md#ref-030) |
| [Dynamic-SUPERB: Towards a dynamic, collaborative, and comprehensive instruction-tuning benchmark for speech](https://doi.org/10.1109/ICASSP48485.2024.10448257) | ICASSP 2024 | [Code](https://github.com/dynamic-superb/dynamic-superb) · [Ref 112](bibliography.md#ref-112) |
| [SpokenWOZ: A large-scale speech-text benchmark for spoken task-oriented dialogue agents](https://proceedings.neurips.cc/paper_files/paper/2023/file/7b16688a2b053a1b01474ab5c78ce662-Paper-Datasets_and_Benchmarks.pdf) | NeurIPS 2023 | [Code](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/spokenwoz) · [Ref 245](bibliography.md#ref-245) |

### Memory and temporal-grounding primitives

These supporting tasks assess retained or temporally localized evidence, without necessarily evaluating a live assistant.

| Paper | Venue | Resources |
| --- | --- | --- |
| [LongMemEval: Benchmarking chat assistants on long-term interactive memory](https://openreview.net/forum?id=pZiyCaVuti) | ICLR 2025 | [Code](https://github.com/xiaowu0162/LongMemEval) · [Ref 290](bibliography.md#ref-290) |
| [Evaluating very long-term conversational memory of LLM agents](https://aclanthology.org/2024.acl-long.747/) | ACL 2024 | [Code](https://github.com/snap-research/locomo) · [Ref 182](bibliography.md#ref-182) |
| [Perception test: A diagnostic benchmark for multimodal video models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8540fba4abdc7f9f7a7b1cc6cd60e409-Abstract.html) | NeurIPS 2023 | [Code](https://github.com/google-deepmind/perception_test) · [Ref 214](bibliography.md#ref-214) |
| [TransRAC: Encoding multi-scale temporal correlation with transformers for repetitive action counting](https://openaccess.thecvf.com/content/CVPR2022/html/Hu_TransRAC_Encoding_Multi-Scale_Temporal_Correlation_With_Transformers_for_Repetitive_Action_CVPR_2022_paper.html) | CVPR 2022 | [Code](https://github.com/SvipRepetitionCounting/TransRAC) · [Ref 109](bibliography.md#ref-109) |
| [Tall: Temporal activity localization via language query](https://doi.org/10.1109/ICCV.2017.563) | ICCV 2017 | [Code](https://github.com/jiyanggao/TALL) · [Ref 89](bibliography.md#ref-089) |
| [Hollywood in homes: Crowdsourcing data collection for activity understanding](https://doi.org/10.1007/978-3-319-46448-0_31) | ECCV 2016 | [Dataset](https://prior.allenai.org/projects/charades) · [Ref 246](bibliography.md#ref-246) |

### Turn-taking and representation primitives

Prediction and tokenizer benchmarks isolate components of a system rather than its complete real-time interaction requirements.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DASB: Discrete audio and speech benchmark](https://openreview.net/forum?id=vGWrp0NjaE) | TMLR 2026 | [Code](https://github.com/speechbrain/benchmarks/tree/main/benchmarks/DASB) · [Ref 193](bibliography.md#ref-193) |
| [MuVAP: Multimodal Multiparty Voice Activity Projection for Turn-taking Prediction in the Wild](https://arxiv.org/abs/2606.16731) | arXiv 2026 | [Code](https://github.com/Haotian-Qi/MuVAP) · [Ref 215](bibliography.md#ref-215) |
| [Talking turns: Benchmarking audio foundation models on turn-taking dynamics](https://proceedings.iclr.cc/paper_files/paper/2025/hash/82f68b38747c406672f7f9f6bab86775-Abstract-Conference.html) | ICLR 2025 | [Code](https://github.com/espnet/espnet/tree/master/egs2/swbd/slu1) · [Ref 10](bibliography.md#ref-010) |
| [Codec-SUPERB @ SLT 2024: A lightweight benchmark for neural audio codec models](https://arxiv.org/abs/2409.14085) | SLT 2024 | [Code](https://github.com/voidful/Codec-SUPERB) · [Ref 292](bibliography.md#ref-292) |
| [STAB: Speech tokenizer assessment benchmark](https://arxiv.org/abs/2409.02384) | arXiv 2024 | [Ref 267](bibliography.md#ref-267) |
| [Voice Activity Projection: Self-supervised Learning of Turn-taking Events](https://www.isca-archive.org/interspeech_2022/ekstedt22_interspeech.html) | Interspeech 2022 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 68](bibliography.md#ref-068) |
| [SUPERB: Speech processing universal performance benchmark](https://www.isca-archive.org/interspeech_2021/yang21c_interspeech.html) | Interspeech 2021 | [Code](https://github.com/s3prl/s3prl) · [Ref 288](bibliography.md#ref-288) |
| [TurnGPT: a transformer-based language model for predicting turn-taking in spoken dialog](https://aclanthology.org/2020.findings-emnlp.268/) | EMNLP Findings 2020 | [Code](https://github.com/ErikEkstedt/TurnGPT) · [Ref 67](bibliography.md#ref-067) |

### Safety, privacy and overlap stress tests

Test unsafe input, unintended speakers and leakage together with the timing and content of the response.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Audio jailbreak: An open comprehensive benchmark for jailbreaking large audio-language models](https://aclanthology.org/2026.acl-long.1259/) | ACL 2026 | [Code](https://github.com/mbzuai-nlp/AudioJailbreak) · [Ref 253](bibliography.md#ref-253) |
| [IRAF: Interference-resilient adaptive fusion for noise-robust end-to-end full-duplex spoken dialogue systems](https://arxiv.org/abs/2606.06559) | arXiv 2026 | [Ref 345](bibliography.md#ref-345) |
| [Jalmbench: Benchmarking jailbreak vulnerabilities in audio language models](https://openreview.net/forum?id=DJkQ236C8B) | ICLR 2026 | [Code](https://github.com/sfofgalaxy/JALMBench) · [Ref 210](bibliography.md#ref-210) |
| [Privacy-preserving end-to-end full-duplex speech dialogue models](https://arxiv.org/abs/2603.08179) | arXiv 2026 | [Ref 140](bibliography.md#ref-140) |
| [Protecting bystander privacy via selective hearing in audio LLMs](https://aclanthology.org/2026.acl-long.693/) | ACL 2026 | [Code](https://github.com/Elocinacademia/SelectiveHearing-Bench) · [Ref 332](bibliography.md#ref-332) |
| [Omni-SafetyBench: A Benchmark for Safety Evaluation of Audio-Visual Large Language Models](https://arxiv.org/abs/2508.07173) | arXiv 2025 | [Code](https://github.com/THU-BPM/Omni-SafetyBench) · [Ref 207](bibliography.md#ref-207) |
