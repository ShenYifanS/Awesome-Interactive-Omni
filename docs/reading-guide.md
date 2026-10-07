# 🧭 Reading guide

[← Home](../README.md) · [Glossary](glossary.md) · [Bibliography](bibliography.md)

Choose the question closest to your work.

| Your starting point | Read in this order | What to look for |
| --- | --- | --- |
| **New to the field** | [Real-time interaction requirements](../README.md#interaction-contract) → [dGSLM](bibliography.md#ref-172) → [Moshi](bibliography.md#ref-052) → [Qwen2.5-Omni](bibliography.md#ref-261) → [benchmark guide](benchmarks.md) | Separate modality breadth, streaming output and true in-interaction control. |
| **Full-duplex speech** | [dGSLM](bibliography.md#ref-172) → [SyncLLM](bibliography.md#ref-230) → [Moshi](bibliography.md#ref-052) → [SALMONN-omni](bibliography.md#ref-285) → [FDB](bibliography.md#ref-136) | Track how each representation encodes silence, overlap and switching between listening and speaking. |
| **Omni architecture** | [representations](representations.md) → [Qwen2.5-Omni](bibliography.md#ref-261) → [Qwen3-Omni](bibliography.md#ref-262) → [VITA](bibliography.md#ref-068) → [ROMA](bibliography.md#ref-226) | Ask which new input can influence output that is already in progress. |
| **Reasoning and tools** | [capability preservation](multi-rate.md) → [Stream RAG](bibliography.md#ref-009) → [MoshiRAG](bibliography.md#ref-039) → [STITCH](bibliography.md#ref-037) → [DuplexOmni](bibliography.md#ref-094) | Track delegation, result insertion and whether evidence still matches the live request. |
| **Memory and long sessions** | [LongMemEval](bibliography.md#ref-251) → [EgoMem](bibliography.md#ref-274) → [StreamingVLM](bibliography.md#ref-263) → [StreamArena](bibliography.md#ref-301) | Distinguish remembering old observations from revising obsolete entities, intentions and tasks. |
| **Evaluation design** | [six dimensions](benchmarks.md) → [FDB v1](bibliography.md#ref-136) → [FDB v2](bibliography.md#ref-139) → [FDB v3](bibliography.md#ref-138) → [OmniMMI](bibliography.md#ref-246) → [open problems](open-problems.md) | Identify combinations that are not measured together under a shared protocol. |
| **Data and training** | [training guide](training.md) → [Moshi](bibliography.md#ref-052) → [SyncLLM](bibliography.md#ref-230) → [DuplexGen](bibliography.md#ref-116) → [interactivity alignment](bibliography.md#ref-175) | Distinguish speech scale from supervision for silence, interruption, repair and result coordination. |

## A useful way to annotate each paper

Record its **input/output modalities**, **real-time interaction requirements**, **location of control**, **state update mechanism**, **training supervision**, **evaluated behaviors** and **released resources**.
