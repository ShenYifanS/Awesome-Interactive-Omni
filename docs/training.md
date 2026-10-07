# 🛠️ Data and training

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**How are content, timing and control learned?**

Organizing supervision by the behavior it teaches.

Survey sections: **4.2–4.3**.

## Match data to the behavior

| Data class | Teaches | Not covered |
| --- | --- | --- |
| ASR / TTS corpora | Speech recognition, speech realization and language–speech alignment. | Turn-taking, interruption intent or appropriate silence. |
| Speaker-separated conversations | Overlap, turn transitions and natural timing. | Broad visual grounding or tool coordination. |
| Audiovisual pairs | Cross-modal grounding and temporal association. | Whether an observed event warrants a response. |
| Spoken instructions | Following requests and producing assistant-style answers. | Natural within-turn repair or backchannels. |
| Synthetic interaction traces | Controlled pauses, overlap, interruption and coordination events. | Natural timing distributions across populations and situations. |
| Preferences and policy traces | When to speak, wait, yield or recover. | Content preservation unless it is measured and protected. |
| Foreground–background traces | Delegation, evidence arrival, insertion, cancellation and revalidation. | Reproducibility unless traces and execution conditions are released. |

### Natural conversation and duplex dialogue

Speaker-separated audio preserves turn transitions, backchannels and overlap; record release conditions before reuse.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexChat: Constructing speaker-separated full-duplex dialogue speech at scale for spoken dialogue language modeling](https://arxiv.org/abs/2607.04941) | arXiv 2026 | [Code](https://github.com/sarulab-speech/DuplexChat) · [Ref 198](bibliography.md#ref-198) |
| [Full-duplex interaction in spoken dialogue systems: A comprehensive study from the icassp 2026 HumDial challenge](https://arxiv.org/abs/2604.21406) | arXiv 2026 | [Code](https://github.com/ASLP-lab/HumDial-FDBench) · [Ref 271](bibliography.md#ref-271) |
| [Open-source full-duplex conversational datasets for natural and interactive speech synthesis](https://doi.org/10.3724/2096-7004.di.2026.00d2) | Data Intelligence 2026 | [Dataset](https://magichub.com/datasets/multi-stream-spontaneous-conversation-training-datasets_english/) · [Ref 347](bibliography.md#ref-347) |
| [Dialospeech: Dual-speaker dialogue generation with LLM and flow matching](https://doi.org/10.1109/APSIPAASC65261.2025.11249327) | APSIPA ASC 2025 | [Project](https://tiamojames.github.io/DialoSpeech/) · [Ref 296](bibliography.md#ref-296) |
| [The fisher corpus: a resource for the next generations of speech-to-text](https://aclanthology.org/L04-1500/) | LREC 2004 | [Dataset](https://catalog.ldc.upenn.edu/LDC2004S13) · [Ref 51](bibliography.md#ref-051) |
| [CALLHOME Collection in Six Languages](https://linguistlist.org/issues/8/1209/) | 1997 | [Ref 169](bibliography.md#ref-169) |
| [Switchboard: telephone speech corpus for research and development](https://doi.org/10.1109/ICASSP.1992.225858) | ICASSP 1992 | [Dataset](https://catalog.ldc.upenn.edu/LDC97S62) · [Ref 93](bibliography.md#ref-093) |

### Speech perception and generation corpora

Foundational speech data supplies recognition and generation capability; dataset names and scales depend on the release.

| Paper | Venue | Resources |
| --- | --- | --- |
| [GigaSpeech 2: An evolving, large-scale and multi-domain ASR corpus for low-resource languages with automated crawling, transcription and refinement](https://aclanthology.org/2025.acl-long.135/) | ACL 2025 | [Code](https://github.com/SpeechColab/GigaSpeech2) · [Ref 308](bibliography.md#ref-308) |
| [Emilia: An extensive, multilingual, and diverse speech dataset for large-scale speech generation](https://arxiv.org/abs/2407.05361) | SLT 2024 | [Code](https://github.com/open-mmlab/Amphion/tree/main/preprocessors/Emilia) · [Ref 103](bibliography.md#ref-103) |
| [Fish-Speech: Leveraging large language models for advanced multilingual text-to-speech synthesis](https://arxiv.org/abs/2411.01156) | arXiv 2024 | [Code](https://github.com/fishaudio/fish-speech) · [Ref 159](bibliography.md#ref-159) |
| [LibriHeavy: a 50,000 hours ASR corpus with punctuation casing and context](https://arxiv.org/abs/2309.08105) | ICASSP 2024 | [Code](https://github.com/k2-fsa/libriheavy) · [Ref 132](bibliography.md#ref-132) |
| [WavCaps: A chatgpt-assisted weakly-labelled audio captioning dataset for audio-language multimodal research](http://dx.doi.org/10.1109/TASLP.2024.3419446) | IEEE TASLP 2024 | [Code](https://github.com/XinhaoMei/WavCaps) · [Ref 185](bibliography.md#ref-185) |
| [WenetSpeech4TTS: A 12,800-hour mandarin TTS corpus for large speech generation model benchmark](https://www.isca-archive.org/interspeech_2024/ma24d_interspeech.html) | Interspeech 2024 | [Code](https://github.com/dukGuo/valle-audiodec) · [Ref 178](bibliography.md#ref-178) |
| [LibriTTS-R: A restored multi-speaker text-to-speech corpus](https://www.isca-archive.org/interspeech_2023/koizumi23_interspeech.html) | Interspeech 2023 | [Dataset](https://www.openslr.org/141/) · [Ref 138](bibliography.md#ref-138) |
| [Yodas: Youtube-oriented dataset for audio and speech](https://arxiv.org/abs/2406.00899) | ASRU 2023 | [Dataset](https://huggingface.co/datasets/espnet/yodas) · [Ref 154](bibliography.md#ref-154) |
| [WenetSpeech: A 10000+ hours multi-domain mandarin corpus for speech recognition](https://arxiv.org/abs/2110.03370) | ICASSP 2022 | [Code](https://github.com/wenet-e2e/WenetSpeech) · [Ref 333](bibliography.md#ref-333) |
| [GigaSpeech: An evolving, multi-domain ASR corpus with 10,000 hours of transcribed audio](http://dx.doi.org/10.21437/Interspeech.2021-1965) | Interspeech 2021 | [Code](https://github.com/SpeechColab/GigaSpeech) · [Ref 33](bibliography.md#ref-033) |
| [The people’s speech: A large-scale diverse english speech recognition dataset for commercial usage](https://datasets-benchmarks-proceedings.neurips.cc/paper_files/paper/2021/hash/202cb962ac59075b964b07152d234b70-Abstract-round1.html) | NeurIPS 2021 | [Code](https://github.com/mlcommons/peoples-speech) · [Ref 88](bibliography.md#ref-088) |
| [VoxPopuli: A large-scale multilingual speech corpus for representation learning, semi-supervised learning and interpretation](https://aclanthology.org/2021.acl-long.80/) | ACL 2021 | [Code](https://github.com/facebookresearch/voxpopuli) · [Ref 269](bibliography.md#ref-269) |
| [Common voice: A massively-multilingual speech corpus](https://aclanthology.org/2020.lrec-1.520/) | LREC 2020 | [Code](https://github.com/common-voice/common-voice) · [Ref 8](bibliography.md#ref-008) |
| [Libri-Light: A benchmark for ASR with limited or no supervision](http://dx.doi.org/10.1109/ICASSP40776.2020.9052942) | ICASSP 2020 | [Code](https://github.com/facebookresearch/libri-light) · [Ref 131](bibliography.md#ref-131) |
| [Mls: A large-scale multilingual dataset for speech research](http://dx.doi.org/10.21437/Interspeech.2020-2826) | Interspeech 2020 | [Dataset](https://www.openslr.org/94/) · [Ref 213](bibliography.md#ref-213) |
| [LibriTTS: A corpus derived from librispeech for text-to-speech](https://www.isca-archive.org/interspeech_2019/zen19_interspeech.html) | Interspeech 2019 | [Dataset](https://www.openslr.org/60/) · [Ref 327](bibliography.md#ref-327) |
| [Librispeech: An ASR corpus based on public domain audio books](https://doi.org/10.1109/ICASSP.2015.7178964) | ICASSP 2015 | [Dataset](https://www.openslr.org/12) · [Ref 208](bibliography.md#ref-208) |

### Audiovisual grounding

Time-aligned audio and video teach what happened and when, but may lack response-policy annotations.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Perception test: A diagnostic benchmark for multimodal video models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8540fba4abdc7f9f7a7b1cc6cd60e409-Abstract.html) | NeurIPS 2023 | [Code](https://github.com/google-deepmind/perception_test) · [Ref 214](bibliography.md#ref-214) |
| [Ego4D: Around the world in 3,000 hours of egocentric video](https://openaccess.thecvf.com/content/CVPR2022/html/Grauman_Ego4D_Around_the_World_in_3000_Hours_of_Egocentric_Video_CVPR_2022_paper.html) | CVPR 2022 | [Code](https://github.com/facebookresearch/Ego4d) · [Ref 97](bibliography.md#ref-097) |
| [The benefit of temporally-strong labels in audio event classification](https://arxiv.org/abs/2105.07031) | ICASSP 2021 | [Dataset](https://research.google.com/audioset/download_strong.html) · [Ref 104](bibliography.md#ref-104) |
| [HowTo100M: Learning a Text-Video Embedding by Watching Hundred Million Narrated Video Clips](https://openaccess.thecvf.com/content_ICCV_2019/html/Miech_HowTo100M_Learning_a_Text-Video_Embedding_by_Watching_Hundred_Million_Narrated_ICCV_2019_paper.html) | ICCV 2019 | [Code](https://github.com/antoine77340/howto100m) · [Ref 188](bibliography.md#ref-188) |
| [Looking to listen at the cocktail party: a speaker-independent audio-visual model for speech separation](http://dx.doi.org/10.1145/3197517.3201357) | ACM TOG 2018 | [Project](https://looking-to-listen.github.io/) · [Ref 71](bibliography.md#ref-071) |
| [VoxCeleb2: Deep speaker recognition](http://dx.doi.org/10.21437/Interspeech.2018-1929) | Interspeech 2018 | [Code](https://github.com/a-nagrani/VGGVox) · [Ref 49](bibliography.md#ref-049) |
| [VoxCeleb: A Large-Scale Speaker Identification Dataset](https://www.isca-archive.org/interspeech_2017/nagrani17_interspeech.html) | Interspeech 2017 | [Code](https://github.com/a-nagrani/VGGVox) · [Ref 196](bibliography.md#ref-196) |

### Instruction and synthetic interaction data

Synthetic instructions and temporal traces offer different supervision: response content versus the timing of interaction events.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexGen: Adaptive synthesis of human-ai turn-taking dialogues](https://arxiv.org/abs/2607.26178) | EMNLP 2026 | [Code](https://github.com/duplexgen/duplexgen-code) · [Ref 137](bibliography.md#ref-137) |
| [DuplexOmni: Real-time listening, seeing, thinking, and speaking for full-duplex interaction](https://arxiv.org/abs/2606.09186) | arXiv 2026 | [Code](https://github.com/MuyeHuang/DuplexOmni) · [Ref 114](bibliography.md#ref-114) |
| [LLaMA-Omni 2: LLM-Based Real-Time Spoken Chatbot with Autoregressive Streaming Speech Synthesis](https://aclanthology.org/2025.acl-long.912/) | ACL 2025 | [Code](https://github.com/ictnlp/LLaMA-Omni2) · [Ref 73](bibliography.md#ref-073) |
| [LLaMA-Omni: Seamless speech interaction with large language models](https://openreview.net/forum?id=PYmrUQmMEw) | ICLR 2025 | [Code](https://github.com/ictnlp/LLaMA-Omni) · [Ref 72](bibliography.md#ref-072) |
| [OmniFlatten: An end-to-end GPT model for seamless voice conversation](https://aclanthology.org/2025.acl-long.709/) | ACL 2025 | [Project](https://omniflatten.github.io/) · [Ref 340](bibliography.md#ref-340) |
| [AnyGPT: Unified multimodal LLM with discrete sequence modeling](https://aclanthology.org/2024.acl-long.521/) | ACL 2024 | [Code](https://github.com/OpenMOSS/AnyGPT) · [Ref 331](bibliography.md#ref-331) |
| [Beyond turn-based interfaces: Synchronous LLMs as full-duplex dialogue agents](https://aclanthology.org/2024.emnlp-main.1192/) | EMNLP 2024 | [Project](https://syncllm.cs.washington.edu/) · [Ref 268](bibliography.md#ref-268) |
| [Mini-Omni: Language models can hear, talk while thinking in streaming](https://arxiv.org/abs/2408.16725) | arXiv 2024 | [Code](https://github.com/gpt-omni/mini-omni) · [Ref 297](bibliography.md#ref-297) |
| [Moshi: a speech-text foundation model for real-time dialogue](https://doi.org/10.48550/arXiv.2410.00037) | arXiv 2024 | [Code](https://github.com/kyutai-labs/moshi) · [Ref 59](bibliography.md#ref-059) |
| [Enhancing chat language models by scaling high-quality instructional conversations](https://aclanthology.org/2023.emnlp-main.183/) | EMNLP 2023 | [Code](https://github.com/thunlp/UltraChat) · [Ref 63](bibliography.md#ref-063) |
| [OpenHermes 2.5: An open dataset of synthetic data for generalist LLM assistants](https://huggingface.co/datasets/teknium/OpenHermes-2.5) | 2023 | [Ref 261](bibliography.md#ref-261) |
| [SpeechGPT: Empowering large language models with intrinsic cross-modal conversational abilities](https://aclanthology.org/2023.findings-emnlp.1055/) | EMNLP Findings 2023 | [Code](https://github.com/0nutation/SpeechGPT) · [Ref 334](bibliography.md#ref-334) |
| [Stanford Alpaca: An instruction-following Llama model](https://github.com/tatsu-lab/stanford_alpaca) | 2023 | [Code](https://github.com/tatsu-lab/stanford_alpaca) · [Ref 260](bibliography.md#ref-260) |

### Content, timing and preference objectives

Separate linguistic quality, speech generation and turn-control objectives so that gains on one axis can be checked against losses on another.

| Paper | Venue | Resources |
| --- | --- | --- |
| [ASPIRin: Action space projection for interactivity-optimized reinforcement learning in full-duplex speech language models](https://arxiv.org/abs/2604.10065) | arXiv 2026 | [Ref 107](bibliography.md#ref-107) |
| [Decoupling conversational dynamics in full-duplex spoken models through reinforcement learning](https://arxiv.org/abs/2607.07148) | arXiv 2026 | [Ref 158](bibliography.md#ref-158) |
| [Multi-faceted interactivity alignment in full-duplex speech models](https://arxiv.org/abs/2606.11167) | EMNLP 2026 | [Model](https://huggingface.co/kyutai/personaplex-rl-seamless) · [Ref 202](bibliography.md#ref-202) |
| [Optimizing conversational quality in spoken dialogue systems with reinforcement learning from AI feedback](https://aclanthology.org/2026.findings-acl.2040/) | ACL Findings 2026 | [Ref 12](bibliography.md#ref-012) |
| [Toward cognitive supersensing in multimodal large language model](https://arxiv.org/abs/2602.01541) | arXiv 2026 | [Code](https://github.com/PediaMedAI/Cognition-MLLM) · [Ref 151](bibliography.md#ref-151) |
| [Align-SLM: Textless spoken language models with reinforcement learning from AI feedback](https://aclanthology.org/2025.acl-long.997/) | ACL 2025 | [Ref 162](bibliography.md#ref-162) |
| [Fine-grained preference optimization improves spatial reasoning in VLMs](https://proceedings.neurips.cc/paper_files/paper/2025/hash/1a17a06de88cf77f25cda0da91615a54-Abstract-Conference.html) | NeurIPS 2025 | [Code](https://github.com/PLAN-Lab/SpatialReasonerR1) · [Ref 239](bibliography.md#ref-239) |
| [Qwen2.5-Omni technical report](https://arxiv.org/abs/2503.20215) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen2.5-Omni) · [Ref 300](bibliography.md#ref-300) |
| [SALMONN-omni: A codec-free LLM for full-duplex speech understanding and generation](https://arxiv.org/abs/2411.18138) | arXiv 2024 | [Code](https://github.com/bytedance/SALMONN) · [Ref 323](bibliography.md#ref-323) |
| [SpeechAlign: Aligning speech generation to human preferences](https://proceedings.neurips.cc/paper_files/paper/2024/hash/5a016da670821af25f151f523a2e563f-Abstract-Conference.html) | NeurIPS 2024 | [Code](https://github.com/0nutation/SpeechGPT) · [Ref 335](bibliography.md#ref-335) |
| [Direct preference optimization: Your language model is secretly a reward model](https://proceedings.neurips.cc/paper_files/paper/2023/hash/a85b405ed65c6477a4fe8302b5e06ce7-Abstract-Conference.html) | NeurIPS 2023 | [Code](https://github.com/eric-mitchell/direct-preference-optimization) · [Ref 224](bibliography.md#ref-224) |

### Reasoning and coordination supervision

Training traces should expose thinking, delegation, result arrival and changes to the current request.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexOmni: Real-time listening, seeing, thinking, and speaking for full-duplex interaction](https://arxiv.org/abs/2606.09186) | arXiv 2026 | [Code](https://github.com/MuyeHuang/DuplexOmni) · [Ref 114](bibliography.md#ref-114) |
| [STITCH: Simultaneous thinking and talking with chunked reasoning for spoken language models](https://openreview.net/forum?id=5Z1eMhCeTb) | ICLR 2026 | [Code](https://github.com/d223302/STITCH) · [Ref 45](bibliography.md#ref-045) |
| [Stream rag: Instant and accurate spoken dialogue systems with streaming tool usage](https://arxiv.org/abs/2510.02044) | ICML 2026 | [Ref 11](bibliography.md#ref-011) |
| [The silent thought: Modeling internal cognition in full-duplex spoken dialogue models via latent reasoning](https://arxiv.org/abs/2603.17837) | ICML 2026 | [Ref 291](bibliography.md#ref-291) |
| [EgoMem: Lifelong memory agent for full-duplex omnimodal models](https://arxiv.org/abs/2509.11914) | arXiv 2025 | [Ref 313](bibliography.md#ref-313) |
