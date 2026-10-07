# 🌊 Streaming representations

[← Home](../README.md) · [Reading guide](reading-guide.md) · [All references](bibliography.md)

**What must a live stream preserve?**

Time, silence, overlap and partial intent carry control information as well as content. The representation sets the update rate, the evidence visible to the model and the cost of keeping multiple streams active.

Survey sections: **3**.

## Preserve the right information

| Representation choice | Main question |
| --- | --- |
| Continuous acoustic features | Which prosodic and non-verbal cues survive the encoder? |
| Semantic speech units | Which linguistic distinctions remain, and which acoustic details are removed? |
| Codec tokens | What fidelity and token-rate budget are required for incremental speech? |
| Video frames and compressed memory | Can current events and older evidence still be temporally grounded? |
| Shared time grid or time IDs | How are heterogeneous update rates, silence and overlap aligned? |
| Tool and reasoning streams | What provenance and request version accompany an asynchronous return? |

### Audio features and semantic units

Continuous features and semantic units trade acoustic detail, linguistic abstraction and token rate.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Codec does matter: Exploring the semantic shortcoming of codec for audio language model](https://ojs.aaai.org/index.php/AAAI/article/view/34761) | AAAI 2025 | [Code](https://github.com/zhenye234/xcodec) · [Ref 315](bibliography.md#ref-315) |
| [Speech discrete tokens or continuous features? a comparative analysis for spoken language understanding in SpeechLLMs](https://aclanthology.org/2025.emnlp-main.1266/) | EMNLP 2025 | [Ref 273](bibliography.md#ref-273) |
| [A comparative study of discrete speech tokens for semantic-related tasks with large language models](https://arxiv.org/abs/2411.08742) | arXiv 2024 | [Ref 272](bibliography.md#ref-272) |
| [dMel: Speech tokenization made simple](https://arxiv.org/abs/2407.15835) | arXiv 2024 | [Code](https://github.com/apple/dmel) · [Ref 18](bibliography.md#ref-018) |
| [WavLM: Large-Scale Self-Supervised Pre-Training for Full Stack Speech Processing](http://dx.doi.org/10.1109/JSTSP.2022.3188113) | IEEE JSTSP 2022 | [Code](https://github.com/microsoft/unilm/tree/master/wavlm) · [Ref 35](bibliography.md#ref-035) |
| [HuBERT: Self-supervised speech representation learning by masked prediction of hidden units](https://doi.org/10.1109/TASLP.2021.3122291) | IEEE TASLP 2021 | [Code](https://github.com/facebookresearch/fairseq/tree/main/examples/hubert) · [Ref 108](bibliography.md#ref-108) |
| [w2v-bert: Combining contrastive learning and masked language modeling for self-supervised speech pre-training](https://arxiv.org/abs/2108.06209) | ASRU 2021 | [Ref 50](bibliography.md#ref-050) |
| [vq-wav2vec: Self-supervised learning of discrete speech representations](https://iclr.cc/virtual_2020/poster_rylwJxrYDS.html) | ICLR 2020 | [Code](https://github.com/facebookresearch/fairseq/tree/main/examples/wav2vec) · [Ref 15](bibliography.md#ref-015) |
| [wav2vec 2.0: A framework for self-supervised learning of speech representations](https://proceedings.neurips.cc/paper/2020/hash/92d1e1eb1cd6f9fba3227870bb6d7f07-Abstract.html) | NeurIPS 2020 | [Code](https://github.com/facebookresearch/fairseq/tree/main/examples/wav2vec) · [Ref 16](bibliography.md#ref-016) |
| [Representation learning with contrastive predictive coding](https://arxiv.org/abs/1807.03748) | arXiv 2018 | [Ref 266](bibliography.md#ref-266) |

### Neural codecs and speech generation

Codecs and output schedules determine fidelity, bandwidth and the rate at which spoken output can be revised.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Autoregressive speech synthesis without vector quantization](https://aclanthology.org/2025.acl-long.65/) | ACL 2025 | [Project](https://www.microsoft.com/en-us/research/project/vall-e-x/melle/) · [Ref 186](bibliography.md#ref-186) |
| [Neural codec language models are zero-shot text to speech synthesizers](https://doi.org/10.1109/TASLPRO.2025.3530270) | IEEE TASLP 2025 | [Ref 36](bibliography.md#ref-036) |
| [TS3-Codec: Transformer-based simple streaming single codec](https://www.isca-archive.org/interspeech_2025/wu25f_interspeech.html) | Interspeech 2025 | [Ref 293](bibliography.md#ref-293) |
| [WavTokenizer: An efficient acoustic discrete codec tokenizer for audio language modeling](https://proceedings.iclr.cc/paper_files/paper/2025/hash/ea1f5f0878d43ff4fb8bf64ef4a2326c-Abstract-Conference.html) | ICLR 2025 | [Code](https://github.com/jishengpeng/WavTokenizer) · [Ref 124](bibliography.md#ref-124) |
| [BigCodec: Pushing the limits of low-bitrate neural speech codec](https://arxiv.org/abs/2409.05377) | arXiv 2024 | [Code](https://github.com/Aria-K-Alethia/BigCodec) · [Ref 299](bibliography.md#ref-299) |
| [NaturalSpeech 3: Zero-shot speech synthesis with factorized codec and diffusion models](https://proceedings.mlr.press/v235/ju24b.html) | ICML 2024 | [Code](https://github.com/open-mmlab/Amphion/tree/main/models/codec/ns3_codec) · [Ref 130](bibliography.md#ref-130) |
| [SNAC: Multi-scale neural audio codec](https://openreview.net/forum?id=PFBF5ctj4X) | NeurIPS Workshop 2024 | [Code](https://github.com/hubertsiuzdak/snac) · [Ref 249](bibliography.md#ref-249) |
| [SpeechTokenizer: Unified speech tokenizer for speech language models](https://openreview.net/forum?id=AF9Q8Vip84) | ICLR 2024 | [Code](https://github.com/ZhangXInFD/SpeechTokenizer) · [Ref 342](bibliography.md#ref-342) |
| [Vocos: Closing the gap between time-domain and fourier-based neural vocoders for high-quality audio synthesis](https://openreview.net/forum?id=vY9nzQmQBw) | ICLR 2024 | [Code](https://github.com/gemelo-ai/vocos) · [Ref 248](bibliography.md#ref-248) |
| [AudioLM: A language modeling approach to audio generation](https://doi.org/10.1109/TASLP.2023.3288409) | IEEE TASLP 2023 | [Project](https://google-research.github.io/seanet/audiolm/examples/) · [Ref 23](bibliography.md#ref-023) |
| [HiFi-Codec: Group-residual vector quantization for high fidelity audio codec](https://arxiv.org/abs/2305.02765) | arXiv 2023 | [Code](https://github.com/yangdongchao/AcademiCodec) · [Ref 306](bibliography.md#ref-306) |
| [High fidelity neural audio compression](https://openreview.net/forum?id=ivCd8z8zR2) | TMLR 2023 | [Code](https://github.com/facebookresearch/encodec) · [Ref 58](bibliography.md#ref-058) |
| [High-fidelity audio compression with improved RVQGAN](https://proceedings.neurips.cc/paper_files/paper/2023/hash/58d0e78cf042af5876e12661087bea12-Abstract-Conference.html) | NeurIPS 2023 | [Code](https://github.com/descriptinc/descript-audio-codec) · [Ref 139](bibliography.md#ref-139) |
| [SoundStream: An end-to-end neural audio codec](https://doi.org/10.1109/TASLP.2021.3129994) | IEEE TASLP 2022 | [Project](https://google-research.github.io/seanet/soundstream/examples/) · [Ref 325](bibliography.md#ref-325) |

### Video streams and temporal compression

Retain the evidence needed for causal understanding while controlling visual-token and cache growth.

| Paper | Venue | Resources |
| --- | --- | --- |
| [StreamingVLM: Real-Time Understanding for Infinite Video Streams](https://openreview.net/forum?id=gVbPWbA97s) | ICLR 2026 | [Code](https://github.com/mit-han-lab/streaming-vlm) · [Ref 302](bibliography.md#ref-302) |
| [Adaptive keyframe sampling for long video understanding](https://openaccess.thecvf.com/content/CVPR2025/html/Tang_Adaptive_Keyframe_Sampling_for_Long_Video_Understanding_CVPR_2025_paper.html) | CVPR 2025 | [Code](https://github.com/ncTimTang/AKS) · [Ref 257](bibliography.md#ref-257) |
| [Flash-VStream: Efficient Real-Time Understanding for Long Video Streams](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Flash-VStream_Efficient_Real-Time_Understanding_for_Long_Video_Streams_ICCV_2025_paper.html) | ICCV 2025 | [Code](https://github.com/IVGSZ/Flash-VStream) · [Ref 337](bibliography.md#ref-337) |
| [Grounded-VideoLLM: Sharpening fine-grained temporal grounding in video large language models](https://aclanthology.org/2025.findings-emnlp.50/) | EMNLP Findings 2025 | [Code](https://github.com/WHB139426/Grounded-Video-LLM) · [Ref 275](bibliography.md#ref-275) |
| [TimeChat-Online: 80% visual tokens are naturally redundant in streaming videos](https://doi.org/10.1145/3746027.3754839) | ACM MM 2025 | [Code](https://github.com/yaolinli/TimeChat-Online) · [Ref 311](bibliography.md#ref-311) |
| [VideoRoPE: What makes for good video rotary position embedding?](https://proceedings.mlr.press/v267/wei25h.html) | ICML 2025 | [Code](https://github.com/Wiselnn570/VideoRoPE) · [Ref 287](bibliography.md#ref-287) |
| [LLaMA-VID: An image is worth 2 tokens in large language models](https://link.springer.com/chapter/10.1007/978-3-031-72952-2_19) | ECCV 2024 | [Code](https://github.com/JIA-Lab-research/LLaMA-VID) · [Ref 156](bibliography.md#ref-156) |
| [Motion2VecSets: 4D Latent Vector Set Diffusion for Non-rigid Shape Reconstruction and Tracking](https://openaccess.thecvf.com/content/CVPR2024/html/Cao_Motion2VecSets_4D_Latent_Vector_Set_Diffusion_for_Non-rigid_Shape_Reconstruction_CVPR_2024_paper.html) | CVPR 2024 | [Ref 27](bibliography.md#ref-027) |
| [TimeChat: A time-sensitive multimodal large language model for long video understanding](https://openaccess.thecvf.com/content/CVPR2024/html/Ren_TimeChat_A_Time-sensitive_Multimodal_Large_Language_Model_for_Long_Video_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/RenShuhuai-Andy/TimeChat) · [Ref 225](bibliography.md#ref-225) |
| [VideoLLM-online: Online video large language model for streaming video](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_VideoLLM-online_Online_Video_Large_Language_Model_for_Streaming_Video_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/showlab/VideoLLM-online) · [Ref 34](bibliography.md#ref-034) |
| [VTimeLLM: Empower LLM to grasp video moments](https://openaccess.thecvf.com/content/CVPR2024/html/Huang_VTimeLLM_Empower_LLM_to_Grasp_Video_Moments_CVPR_2024_paper.html) | CVPR 2024 | [Code](https://github.com/huangb23/VTimeLLM) · [Ref 111](bibliography.md#ref-111) |
| [Token merging: Your ViT but faster](https://openreview.net/forum?id=JroZRaRw7Eu) | ICLR 2023 | [Code](https://github.com/facebookresearch/ToMe) · [Ref 22](bibliography.md#ref-022) |
| [Perceiver IO: A General Architecture for Structured Inputs and Outputs](https://openreview.net/forum?id=fILj7WpI-g) | ICLR 2022 | [Ref 121](bibliography.md#ref-121) |
| [Perceiver: General Perception with Iterative Attention](https://proceedings.mlr.press/v139/jaegle21a.html) | ICML 2021 | [Ref 120](bibliography.md#ref-120) |

### Time, silence and overlap

Represent conversational timing explicitly, including intervals in which waiting is the correct action.

| Paper | Venue | Resources |
| --- | --- | --- |
| [Streaming sequence-to-sequence learning with delayed streams modeling](https://arxiv.org/abs/2509.08753) | arXiv 2025 | [Code](https://github.com/kyutai-labs/delayed-streams-modeling) · [Ref 326](bibliography.md#ref-326) |
| [Beyond turn-based interfaces: Synchronous LLMs as full-duplex dialogue agents](https://aclanthology.org/2024.emnlp-main.1192/) | EMNLP 2024 | [Project](https://syncllm.cs.washington.edu/) · [Ref 268](bibliography.md#ref-268) |
| [Real-time and continuous turn-taking prediction using voice activity projection](https://arxiv.org/abs/2401.04868) | IWSDS 2024 | [Code](https://github.com/inokoj/VAP-Realtime) · [Ref 117](bibliography.md#ref-117) |
| [Speech ReaLLM -- Real-time Speech Recognition with Multimodal Language Models by Teaching the Flow of Time](https://www.isca-archive.org/interspeech_2024/seide24_interspeech.html) | Interspeech 2024 | [Ref 236](bibliography.md#ref-236) |
| [Generative spoken dialogue language modeling](https://aclanthology.org/2023.tacl-1.15/) | TACL 2023 | [Code](https://github.com/facebookresearch/fairseq/tree/main/examples/textless_nlp/dgslm) · [Ref 199](bibliography.md#ref-199) |
| [What makes a good pause? investigating the turn-holding effects of fillers](https://www.internationalphoneticassociation.org/icphs-proceedings/ICPhS2023/full_papers/828.pdf) | ICPhS 2023 | [Code](https://github.com/ErikEkstedt/vap_fillers) · [Ref 126](bibliography.md#ref-126) |
| [How much does prosody help turn-taking? investigations using voice activity projection models](https://aclanthology.org/2022.sigdial-1.51/) | SIGDIAL 2022 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 69](bibliography.md#ref-069) |
| [Voice Activity Projection: Self-supervised Learning of Turn-taking Events](https://www.isca-archive.org/interspeech_2022/ekstedt22_interspeech.html) | Interspeech 2022 | [Code](https://github.com/ErikEkstedt/VoiceActivityProjection) · [Ref 68](bibliography.md#ref-068) |
| [TurnGPT: a transformer-based language model for predicting turn-taking in spoken dialog](https://aclanthology.org/2020.findings-emnlp.268/) | EMNLP Findings 2020 | [Code](https://github.com/ErikEkstedt/TurnGPT) · [Ref 67](bibliography.md#ref-067) |

### Unified streams and asynchronous results

Speech, text, visual updates and tool results need compatible temporal interfaces and provenance.

| Paper | Venue | Resources |
| --- | --- | --- |
| [DuplexOmni: Real-time listening, seeing, thinking, and speaking for full-duplex interaction](https://arxiv.org/abs/2606.09186) | arXiv 2026 | [Code](https://github.com/MuyeHuang/DuplexOmni) · [Ref 114](bibliography.md#ref-114) |
| [STITCH: Simultaneous thinking and talking with chunked reasoning for spoken language models](https://openreview.net/forum?id=5Z1eMhCeTb) | ICLR 2026 | [Code](https://github.com/d223302/STITCH) · [Ref 45](bibliography.md#ref-045) |
| [Stream rag: Instant and accurate spoken dialogue systems with streaming tool usage](https://arxiv.org/abs/2510.02044) | ICML 2026 | [Ref 11](bibliography.md#ref-011) |
| [Qwen2.5-Omni technical report](https://arxiv.org/abs/2503.20215) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen2.5-Omni) · [Ref 300](bibliography.md#ref-300) |
| [Qwen3-Omni technical report](https://arxiv.org/abs/2509.17765) | arXiv 2025 | [Code](https://github.com/QwenLM/Qwen3-Omni) · [Ref 301](bibliography.md#ref-301) |
| [SpiRit-LM: Interleaved spoken and written language model](https://aclanthology.org/2025.tacl-1.2/) | TACL 2025 | [Code](https://github.com/facebookresearch/spiritlm) · [Ref 200](bibliography.md#ref-200) |
| [AnyGPT: Unified multimodal LLM with discrete sequence modeling](https://aclanthology.org/2024.acl-long.521/) | ACL 2024 | [Code](https://github.com/OpenMOSS/AnyGPT) · [Ref 331](bibliography.md#ref-331) |
| [Interleaved speech-text language models for simple streaming text-to-speech synthesis](https://arxiv.org/abs/2412.16102) | arXiv 2024 | [Ref 307](bibliography.md#ref-307) |
| [VoxtLM: Unified decoder-only models for consolidating speech recognition, synthesis and speech, text continuation tasks](https://doi.org/10.1109/ICASSP48485.2024.10447112) | ICASSP 2024 | [Code](https://github.com/espnet/espnet/tree/master/egs2/voxtlm_v1/lm1) · [Ref 184](bibliography.md#ref-184) |
| [WebGPT: Browser-Assisted Question-Answering with Human Feedback](https://arxiv.org/abs/2112.09332) | arXiv 2021 | [Ref 197](bibliography.md#ref-197) |
