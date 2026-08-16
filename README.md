# Javier Ponzo

**Co-Founder & Tech Lead at [Marsstein.ai](https://marsstein.ai)** — privacy-preserving computer
vision for the automotive industry, and the infrastructure that proves it works.

I build detection models, the pipelines that run them at scale, and the agent systems that keep
the whole thing moving. Most of it ships under NDA, so here is what it is rather than where it is.

---

## What I work on

### ADAS footage anonymization

Faces and licence plates removed from driving footage before it ever leaves the EU. YOLOX-m
detection feeding a CUDA mosaic stage on DeepStream, FP16 — **~400 fps on 1080p H.265**. A Rust
inference engine behind a Go orchestration pipeline, ingesting MP4, H.264, H.265 and MCAP.
Every operation lands in a SHA-256 hash-chained audit log, and processing never leaves EU soil.

`Rust` · `Go` · `CUDA` · `DeepStream` · `TensorRT` · `YOLOX` · `PostgreSQL`

### ISA conformity testing — EU Reg. 2019/2144

Every new vehicle sold in the EU must display the correct legal speed limit. Proving it today
costs a test engineer weeks on a DewesoftX rig plus a paid map licence, marking each detection
right or wrong by hand.

We drive the route, establish the legal limit **independently from two sources**, compare both
against what the car actually displayed, and hand a human a short ranked list of the moments
that genuinely need a decision. Their signed verdict becomes the certifiable record. Runs
entirely on-prem.

`Python` · `computer vision` · `sensor fusion` · `regulatory conformity`

### Model training infrastructure

A GPU training fleet defined in code: managed instance groups with preemption handling, ClearML
experiment tracking, ensemble auto-labelling to cut annotation cost, immutable per-phase
archives, and read-only release buckets so production consumes models without ever touching
training resources.

`Go` · `Pulumi` · `ClearML` · `GCP` · `KMS`

### Agent systems & automation

Autonomous planner → coder → verifier loops that run until a real verify command exits 0, with
the verifier deliberately separated from the agent that wrote the code. Multi-agent
orchestration, a 24/7 team bot, and automation across marketing, accounting and document
generation.

`Node.js` · `Python` · `multi-agent orchestration` · `MCP`

---

## Open source

| Project | |
|---|---|
| **[gpu-control](https://github.com/JavierPonzo/gpu-control)** | Native Linux system monitor for developers — GPU, CPU, memory, thermals, power, kernel-level issue detection and updates in one window. Tauri + Rust + React. |
| **[loadingo](https://github.com/JavierPonzo/loadingo)** | Learn a language during AI wait time. Spaced-repetition micro-lessons in a VS Code sidebar that step aside the moment your agent needs you. |

---

## Stack

```
Vision      YOLOX · DeepStream · CUDA · TensorRT · OpenCV
Systems     Rust · Go · Python · TypeScript
Platform    FastAPI · Next.js · PostgreSQL · NATS · Qdrant
Infra       Pulumi · Docker · k3s · Terraform · GCP · Alibaba · Tencent
Practice    EU data residency · audit logging · on-prem deployment
```

## Interests

Privacy-preserving computer vision · EU AI Act and type-approval conformity · multi-agent
orchestration · making regulated ML systems auditable rather than merely accurate.

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/javierponzo)
[![Website](https://img.shields.io/badge/marsstein.ai-1C4A6E?style=flat&logo=safari&logoColor=white)](https://marsstein.ai)
