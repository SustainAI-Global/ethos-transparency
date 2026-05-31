# Architecture — Ethos-32B (public overview)

This document describes the **high-level, public-safe** architecture of Ethos-32B v1. It explains how components fit together without exposing private infrastructure, training commands, or backend implementation details.

For access and deployment policy, see [USAGE.md](USAGE.md).

---

## Design goals

- **Specialist, not generalist** — depth in sustainable economics, energy, finance, and transition policy
- **Hosted stewardship** — safety, updates, and fair access at the serving layer
- **Phased capability** — core language skills first, then tools, routing, and preference alignment
- **Renewable-aware development** — minimize and disclose energy footprint as we scale

---

## Base model and fine-tuning

| Component | Choice |
|-----------|--------|
| Base model | [Qwen/Qwen3-32B-FP8](https://huggingface.co/Qwen/Qwen3-32B-FP8) (Apache 2.0) |
| Adaptation | **QLoRA** fine-tuning on domain-aligned instruction data |
| Product name | **Ethos-32B (ESI)** |

Fine-tuning produces the **core Ethos model** — the specialist weights that encode our alignment themes and domain focus. Weights remain **private** and are served only through our hosted stack (see [USAGE.md](USAGE.md)).

---

## Three layers

```
┌─────────────────────────────────────────────────────────┐
│  Layer 3 — Hosted chat & API (public access surface)    │
│  Invitation / agreements · safety · rate limits         │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│  Layer 2 — Agent layer                                  │
│  Routing · tools · humility / deferral · context          │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│  Layer 1 — Core model (Ethos-32B fine-tuned weights)    │
│  Qwen3-32B-FP8 + QLoRA · ESI alignment                  │
└─────────────────────────────────────────────────────────┘
```

### Layer 1 — Core model

The fine-tuned 32B model is the reasoning engine for ESI behavior: jobs-first framing, systems thinking, care for people and planet, and domain vocabulary for green economics.

### Layer 2 — Agent layer

The agent layer sits above the core model and handles:

- **Tool calling** (where enabled in training phase)
- **Routing** — when to answer, when to narrow scope, when to defer
- **Humility** — surfacing uncertainty and recommending human or expert follow-up

Implementation details of agents and backends are not published in this repository.

### Layer 3 — Hosted chat and API

Users interact only through **hosted chat** (private beta; invitation via [sustainai.global](https://sustainai.global/)) and **API** (signed agreements). There is no public weight download.

---

## Domain focus

Training and evaluation emphasize:

- **Sustainable economics** — growth, distribution, and systems that reward real value
- **Renewable energy** — deployment, grids, storage, and transition pathways
- **Green finance** — risk, disclosure, and capital aligned with climate goals
- **Just transition** — workers, regions, and institutions through structural change

Application-specific products (economics tools, jobs platforms, content workflows) ship in **separate repositories**, not here.

---

## Phased training roadmap

| Phase | Focus | Status (v1) |
|-------|--------|-------------|
| 1 | **Supervised fine-tuning (SFT)** on curated instruction data | In progress / core of v1 |
| 2 | **Tool calling** — structured actions via agent layer | Planned / early integration |
| 3 | **Routing & humility** — deferral, scope limits, escalation | Planned |
| 4 | **Preference alignment (DPO / ORPO)** — later refinement | Future |

Evaluation methodology and published metrics are **forthcoming**; see [MODEL_CARD.md](MODEL_CARD.md).

---

## Data pipeline (public summary)

- Target corpus on the order of **8k–25k** high-quality examples (not millions of noisy rows)
- Mix of **synthetic generation** with **committee review** before inclusion and public release
- Full dataset planned as **`ethos-training-data-v1`** on Hugging Face when published
- Representative samples only in [data/sample/](data/sample/README.md)

See [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) for philosophy and governance.

---

## Development environment (public)

- **Alignment and iteration** on local **solar-powered** development hardware (Mac Mini class)
- **GPU training** requires additional renewable capacity; we are **seeking funding and partners** for renewable GPU hours rather than defaulting to unconstrained fossil-grid burst training

We do not publish cloud provider accounts, internal hostnames, or operational runbooks in this repo.

---

## What we intentionally omit here

The following stay in private development environments:

- Full training scripts and hyperparameter sweeps
- Raw or pre-committee datasets
- Production API keys, secrets, and infra-as-code
- Model checkpoint distribution beyond private Hugging Face storage
- Experiment logs and internal evaluation dashboards

---

## Related documentation

- [README.md](README.md) — Repository overview
- [USAGE.md](USAGE.md) — Access policy
- [MODEL_CARD.md](MODEL_CARD.md) — Model card
- [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) — Training principles
- [config/README.md](config/README.md) — Skeleton config placeholders
- [data/sample/README.md](data/sample/README.md) — Sample data plan

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
