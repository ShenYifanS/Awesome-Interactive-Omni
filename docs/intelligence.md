# 🧠 Maintaining omni intelligence

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**What remains understood as the world changes?**

Interactive intelligence needs evolving temporal grounding, revisable memory and reasoning that can use incomplete evidence. A fluent response is useful only if it stays consistent with the current scene, user intent and available evidence.

Survey sections: **5**.

## State must be revisable

A useful event record keeps the source, time and task relevance of an observation. The interaction state also needs to distinguish what was inferred, what was said, what the user actually heard, and what became obsolete after a correction.

The survey's five coupled capabilities are **temporal grounding**, **memory and session state**, **reasoning and tools**, **factual grounding**, and **social/pragmatic understanding**.

### Temporal grounding and event understanding

Bind objects, actions and speech to the correct moment while new observations arrive.

| Paper | Venue | Resources |
| --- | --- | --- |
| [ChronoVision: Temporal reasoning via latent state reconstruction](https://arxiv.org/abs/2608.05631) | arXiv 2026 | [Ref 241](bibliography.md#ref-241) |
| [FineMoLA: Towards fine-grained motion-language alignment from clip-level supervision](https://openaccess.thecvf.com/content/CVPR2026W/HuMoGen/html/Wang_FineMoLA_Towards_Fine-Grained_Motion-Language_Alignment_from_Clip-Level_Supervision_CVPRW_2026_paper.html) | CVPRW 2026 | [Ref 280](bibliography.md#ref-280) |
| [StreamingBench: Assessing the gap for mllms to achieve streaming video understanding](https://doi.org/10.1109/ICASSP55912.2026.11463959) | ICASSP 2026 | [Code](https://github.com/THUNLP-MT/StreamingBench) · [Ref 166](bibliography.md#ref-166) |
| [StreamingVLM: Real-Time Understanding for Infinite Video Streams](https://openreview.net/forum?id=gVbPWbA97s) | ICLR 2026 | [Code](https://github.com/mit-han-lab/streaming-vlm) · [Ref 302](bibliography.md#ref-302) |
| [Grounded-VideoLLM: Sharpening fine-grained temporal grounding in video large language models](https://aclanthology.org/2025.findings-emnlp.50/) | EMNLP Findings 2025 | [Code](https://github.com/WHB139426/Grounded-Video-LLM) · [Ref 275](bibliography.md#ref-275) |
| [OmniMMI: A comprehensive multi-modal interaction benchmark in streaming video contexts](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_OmniMMI_A_Comprehensive_Multi-modal_Interaction_Benchmark_in_Streaming_Video_Contexts_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/OmniMMI/OmniMMI) · [Ref 284](bibliography.md#ref-284) |
| [Streaming video question-answering with in-context video kv-cache retrieval](https://proceedings.iclr.cc/paper_files/paper/2025/file/67a9b444cbcd647572c88194619f72d5-Paper-Conference.pdf) | ICLR 2025 | [Code](https://github.com/Becomebright/ReKV) · [Ref 61](bibliography.md#ref-061) |
| [VideoLLM knows when to speak: Enhancing time-sensitive video comprehension with video-text duet interaction format](https://aclanthology.org/2025.findings-emnlp.336/) | EMNLP Findings 2025 | [Code](https://github.com/yellow-binary-tree/MMDuet) · [Ref 283](bibliography.md#ref-283) |
| [TimeChat: A time-sensitive multimodal large language model for long video understanding](https://openaccess.thecvf.com/content/CVPR2024/html/Ren_TimeChat_A_Time-sensitive_Multimodal_Large_Language_Model_for_Long_Video_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/RenShuhuai-Andy/TimeChat) · [Ref 225](bibliography.md#ref-225) |
| [VideoLLM-online: Online video large language model for streaming video](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_VideoLLM-online_Online_Video_Large_Language_Model_for_Streaming_Video_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/showlab/VideoLLM-online) · [Ref 34](bibliography.md#ref-034) |
| [VTimeLLM: Empower LLM to grasp video moments](https://openaccess.thecvf.com/content/CVPR2024/html/Huang_VTimeLLM_Empower_LLM_to_Grasp_Video_Moments_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/huangb23/VTimeLLM) · [Ref 111](bibliography.md#ref-111) |

### Memory and session state

Preserve entity identity and task state while allowing corrections and invalidation of obsolete information.

| Paper | Venue | Resources |
| --- | --- | --- |
| [APEX-MEM: Agentic semi-structured memory with temporal reasoning for long-term conversational AI](https://aclanthology.org/2026.acl-long.749/) | ACL 2026 | [Ref 21](bibliography.md#ref-021) |
| [Beyond retrieval: Progressive latent memory evolution for streaming video understanding](https://arxiv.org/abs/2609.04131) | arXiv 2026 | [Ref 220](bibliography.md#ref-220) |
| [MemORAI: Memory organization and retrieval via adaptive graph intelligence for LLM conversational agents](https://aclanthology.org/2026.findings-acl.1408/) | ACL Findings 2026 | [Ref 265](bibliography.md#ref-265) |
| [Scaling the long video understanding of multimodal large language models via visual memory mechanism](https://arxiv.org/abs/2603.29252) | CVPR 2026 | [Code](https://github.com/city1517/FlexMem) · [Ref 39](bibliography.md#ref-039) |
| [STALE: Can LLM agents know when their memories are no longer valid?](https://arxiv.org/abs/2605.06527) | arXiv 2026 | [Ref 32](bibliography.md#ref-032) |
| [StreamArena: Toward continuous, interactive, and long-horizon agentic streaming video understanding](https://arxiv.org/abs/2608.05703) | arXiv 2026 | [Code](https://github.com/JIA-Lab-research/StreamArena) · [Ref 341](bibliography.md#ref-341) |
| [EgoMem: Lifelong memory agent for full-duplex omnimodal models](https://arxiv.org/abs/2509.11914) | arXiv 2025 | [Ref 313](bibliography.md#ref-313) |
| [Flash-VStream: Efficient Real-Time Understanding for Long Video Streams](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Flash-VStream_Efficient_Real-Time_Understanding_for_Long_Video_Streams_ICCV_2025_paper.html) | ICCV 2025 | [Code](https://github.com/IVGSZ/Flash-VStream) · [Ref 337](bibliography.md#ref-337) |
| [HiAgent: Hierarchical working memory management for solving long-horizon agent tasks with large language model](https://aclanthology.org/2025.acl-long.1575/) | ACL 2025 | [Code](https://github.com/HiAgent2024/HiAgent) · [Ref 110](bibliography.md#ref-110) |
| [LongMemEval: Benchmarking chat assistants on long-term interactive memory](https://openreview.net/forum?id=pZiyCaVuti) | ICLR 2025 | [Code](https://github.com/xiaowu0162/LongMemEval) · [Ref 290](bibliography.md#ref-290) |
| [Position: Episodic memory is the missing piece for long-term LLM agents](https://arxiv.org/abs/2502.06975) | arXiv 2025 | [Ref 211](bibliography.md#ref-211) |
| [Evaluating very long-term conversational memory of LLM agents](https://aclanthology.org/2024.acl-long.747/) | ACL 2024 | [Code](https://github.com/snap-research/locomo) · [Ref 182](bibliography.md#ref-182) |
| [Lost in the middle: How language models use long contexts](https://aclanthology.org/2024.tacl-1.9/) | TACL 2024 | [Code](https://github.com/nelson-liu/lost-in-the-middle) · [Ref 173](bibliography.md#ref-173) |
| [The Dialog State Tracking Challenge series: A review](https://aclanthology.org/2016.dnd-7.5/) | Dialogue & Discourse 2016 | [Ref 289](bibliography.md#ref-289) |

### Reasoning and tools under real-time constraints

Reasoning, tool queries and perception may proceed concurrently; returned evidence must still match the current request.

| Paper | Venue | Resources |
| --- | --- | --- |
| [MoshiRAG: Asynchronous knowledge retrieval for full-duplex speech language models](https://icml.cc/virtual/2026/poster/66336) | ICML 2026 | [Code](https://github.com/kyutai-labs/moshi-rag) · [Ref 46](bibliography.md#ref-046) |
| [Multi-turn agentic scientific literature search via workflow induction](https://arxiv.org/abs/2607.00597) | arXiv 2026 | [Code](https://github.com/mtilyxuegao/PaperPilot) · [Ref 152](bibliography.md#ref-152) |
| [SHANKS: Simultaneous hearing and thinking for spoken language models](https://aclanthology.org/2026.acl-long.404/) | ACL 2026 | [Project](https://d223302.github.io/SHANKS/) · [Ref 44](bibliography.md#ref-044) |
| [STITCH: Simultaneous thinking and talking with chunked reasoning for spoken language models](https://openreview.net/forum?id=5Z1eMhCeTb) | ICLR 2026 | [Code](https://github.com/d223302/STITCH) · [Ref 45](bibliography.md#ref-045) |
| [Stream rag: Instant and accurate spoken dialogue systems with streaming tool usage](https://arxiv.org/abs/2510.02044) | ICML 2026 | [Ref 11](bibliography.md#ref-011) |
| [The silent thought: Modeling internal cognition in full-duplex spoken dialogue models via latent reasoning](https://arxiv.org/abs/2603.17837) | ICML 2026 | [Ref 291](bibliography.md#ref-291) |
| [Thinking-while-speaking: A controlled, interleaved reasoning method for real-time speech generation](https://arxiv.org/abs/2605.20946) | arXiv 2026 | [Ref 65](bibliography.md#ref-065) |
| [Video streaming thinking: Videollms can watch and think simultaneously](https://arxiv.org/abs/2603.12262) | ECCV 2026 | [Code](https://github.com/1ranGuan/VST) · [Ref 99](bibliography.md#ref-099) |
| [When does streaming tool use help? characterizing tool-intent stabilization in streaming retrieval-augmented generation](https://arxiv.org/abs/2606.20113) | arXiv 2026 | [Code](https://github.com/elroy-galbraith/stablize_CRAG) · [Ref 86](bibliography.md#ref-086) |
| [Can speech LLMs think while listening?](https://arxiv.org/abs/2510.07497) | arXiv 2025 | [Ref 243](bibliography.md#ref-243) |
| [ToolLLM: Facilitating large language models to master 16000+ real-world APIs](https://proceedings.iclr.cc/paper_files/paper/2024/hash/28e50ee5b72e90b50e7196fde8ea260e-Abstract-Conference.html) | ICLR 2024 | [Code](https://github.com/OpenBMB/ToolBench) · [Ref 217](bibliography.md#ref-217) |
| [ReAct: Synergizing reasoning and acting in language models](https://openreview.net/forum?id=WE_vluYUL-X) | ICLR 2023 | [Code](https://github.com/ysymyth/ReAct) · [Ref 312](bibliography.md#ref-312) |
| [Toolformer: Language models can teach themselves to use tools](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html) | NeurIPS 2023 | [Ref 235](bibliography.md#ref-235) |

### Factual grounding and capability preservation

Compare spoken and interactive capability with the underlying language backbone and track stale or irrelevant evidence.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Closing the gap between text and speech understanding in LLMs](https://openreview.net/forum?id=dDHnO3Vhyj) | ICLR 2026 | [Ref 53](bibliography.md#ref-053) |
| [Diagnosing and mitigating modality interference in multimodal large language models](https://arxiv.org/abs/2505.19616) | arXiv 2026 | [Code](https://github.com/luisrui/Modality-Interference-in-MLLMs) · [Ref 26](bibliography.md#ref-026) |
| [MoST: Mixing speech and text with modality-aware mixture of experts](https://arxiv.org/abs/2601.10272) | arXiv 2026 | [Code](https://github.com/NUS-HPC-AI-Lab/MoST) · [Ref 176](bibliography.md#ref-176) |
| [Understanding textual capability degradation in speech LLMs via parameter importance analysis](https://doi.org/10.1109/ICASSP55912.2026.11461684) | ICASSP 2026 | [Ref 270](bibliography.md#ref-270) |
| [DeepOmni: Towards seamless and smart speech interaction with adaptive modality-specific MoE](https://arxiv.org/abs/2506.21864) | arXiv 2025 | [Code](https://github.com/talkking/DeepTalk) · [Ref 238](bibliography.md#ref-238) |
| [URO-Bench: Towards comprehensive evaluation for end-to-end spoken dialogue models](https://aclanthology.org/2025.findings-emnlp.933/) | EMNLP Findings 2025 | [Code](https://github.com/Ruiqi-Yan/URO-Bench) · [Ref 303](bibliography.md#ref-303) |
| [Self-RAG: Learning to retrieve, generate, and critique through self-reflection](https://proceedings.iclr.cc/paper_files/paper/2024/hash/25f7be9694d7b32d5cc670927b8091e1-Abstract-Conference.html) | ICLR 2024 | [Code](https://github.com/AkariAsai/self-rag) · [Ref 13](bibliography.md#ref-013) |
| [Active retrieval augmented generation](https://aclanthology.org/2023.emnlp-main.495/) | EMNLP 2023 | [Code](https://github.com/jzbjyb/FLARE) · [Ref 128](bibliography.md#ref-128) |
| [Enabling large language models to generate text with citations](https://aclanthology.org/2023.emnlp-main.398/) | EMNLP 2023 | [Code](https://github.com/princeton-nlp/ALCE) · [Ref 90](bibliography.md#ref-090) |
| [Retrieval-augmented generation for knowledge-intensive NLP tasks](https://proceedings.neurips.cc/paper/2020/hash/6b493230205f780e1bc26945df7481e5-Abstract.html) | NeurIPS 2020 | [Model](https://huggingface.co/facebook/rag-token-nq) · [Ref 150](bibliography.md#ref-150) |

### Social and pragmatic understanding

Recognize addressees, backchannels and conversational intent before deciding to take the floor.

| Paper | Venue | Resources |
| --- | --- | --- |
| [MuVAP: Multimodal Multiparty Voice Activity Projection for Turn-taking Prediction in the Wild](https://arxiv.org/abs/2606.16731) | arXiv 2026 | [Code](https://github.com/Haotian-Qi/MuVAP) · [Ref 215](bibliography.md#ref-215) |
| [An LLM benchmark for addressee recognition in multi-modal multi-party dialogue](https://aclanthology.org/2025.iwsds-1.36/) | IWSDS 2025 | [Ref 118](bibliography.md#ref-118) |
| [Yeah, un, oh: Continuous and real-time backchannel prediction with fine-tuning of voice activity projection](https://aclanthology.org/2025.naacl-long.367/) | NAACL 2025 | [Code](https://github.com/MaAI-Kyoto/MaAI) · [Ref 119](bibliography.md#ref-119) |
| [Multilingual turn-taking prediction using voice activity projection](https://aclanthology.org/2024.lrec-main.1036/) | LREC-COLING 2024 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 116](bibliography.md#ref-116) |
| [How much does prosody help turn-taking? investigations using voice activity projection models](https://aclanthology.org/2022.sigdial-1.51/) | SIGDIAL 2022 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 69](bibliography.md#ref-069) |
| [Turn-taking in conversational systems and human-robot interaction: A review](https://www.sciencedirect.com/science/article/pii/S088523082030111X) | Comput. Speech Lang. 2021 | [Ref 251](bibliography.md#ref-251) |
| [Deep Learning Based Multi-modal Addressee Recognition in Visual Scenes with Utterances](https://doi.org/10.24963/ijcai.2018/214) | IJCAI 2018 | [Ref 189](bibliography.md#ref-189) |
| [Universals and cultural variation in turn-taking in conversation](https://www.pnas.org/doi/10.1073/pnas.0903616106) | PNAS 2009 | [Ref 255](bibliography.md#ref-255) |
