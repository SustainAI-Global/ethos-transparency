# Architecture — Ethos ESI (public overview)

This document describes the **high-level, public-safe** architecture of **Ethos ESI** (Ethical Specialized Intelligence) v1. It explains how components fit together without exposing private infrastructure, training commands, provider accounts, or backend implementation details.

**Canonical technical architecture** lives in the private [`ethos-esi`](https://github.com/SustainAI-Global/ethos-esi) repository. This file is a **sanitized public mirror** — update it only when reviewed for release.

For access and deployment policy, see [USAGE.md](USAGE.md).

---

## Design goals

- **Specialist, not generalist** — depth in sustainable economics, energy, finance, and transition policy
- **Composite architecture** — a fine-tuned core model plus an agent layer that can defer on out-of-scope or high-stakes tasks
- **Hosted stewardship** — safety, updates, and fair access at the serving layer
- **Phased capability** — core language skills first, then tools, routing, and preference alignment
- **Renewable-aware development** — minimize and disclose energy footprint as we scale

---

## Product name and base model (public)

| Use | Name |
|-----|------|
| Product / chat / API | **Ethos ESI** |
| Private weights storage | `sustainai-global/ethos-esi` on Hugging Face (not distributed) |

We do **not** put parameter counts in the product name, model card title, or user-facing docs. Ethos ESI is fine-tuned via **QLoRA** on an **open-licensed Qwen3-class base** (Apache 2.0). The specific base size is a technical implementation choice that may change between checkpoint versions without a rebrand.

Fine-tuning produces the **core Ethos model** — the specialist weights that encode the [Ten Principles](CHARTER.md) and domain focus. Weights remain **private** and are served only through our hosted stack (see [USAGE.md](USAGE.md)).

---

## Three layers

End users and external applications interact through the **Ethos API and chat** (Layer 3). They do not call model providers or training infrastructure directly.

```
┌──────────────────────────────────────────────────────────────────────┐
│  Layer 3 — Ethos API & chat (public access surface)                  │
│  Hosted chat · OpenAI-compatible API · auth & rate limits            │
│  → standard interface for beta testers, apps, and signed API clients │
├──────────────────────────────────────────────────────────────────────┤
│  Layer 2 — Agent layer                                               │
│  Skills · tool calling · multi-turn · humility / deferral routing    │
│  → delegates when Ethos is out of scope or evidence is insufficient  │
├──────────────────────────────────────────────────────────────────────┤
│  Layer 1 — Core model (Ethos ESI)                                    │
│  Fine-tuned specialist · Charter · system prompt · LoRA adapter      │
└──────────────────────────────────────────────────────────────────────┘

Clients  →  Ethos API / chat  →  Agent  →  Core model (hosted)
                              ↘  External models when needed (delegation)
```

### Layer 1 — Core model

The fine-tuned Ethos ESI model is the deep domain expert: [Ten Principles](CHARTER.md), jobs-first framing, systems thinking, and vocabulary for green economics, renewable energy, green finance, and just transition.

### Layer 2 — Agent layer

The agent sits between the API and the core model and handles:

- **Skills** — reusable workflows for consistent behavior
- **Tool calling** (where enabled in training phase)
- **Routing** — when to answer, when to narrow scope, when to defer
- **Humility** — surfacing uncertainty and recommending human or expert follow-up
- **Synthesis** — coherent Ethos-voice answers when external models contributed materially

Implementation details of agents, routing policies, and provider integrations are not published in this repository.

### Layer 3 — Ethos API and chat

Users and approved applications connect through **one standard Ethos interface** — not separate provider endpoints.

| Surface | v1 |
|---------|-----|
| **Chat** | Private beta; invitation via [sustainai.global](https://sustainai.global/) |
| **API** | Signed agreements and contracts only |

SustainAI application repos (economics, jobs, content, etc.) live in **separate repositories** and connect via the Ethos API under approved agreements.

---

## Domain focus

Training and evaluation emphasize:

- **Sustainable economics** — growth, distribution, and systems that reward real value
- **Renewable energy** — deployment, grids, storage, and transition pathways
- **Green finance** — risk, disclosure, and capital aligned with climate goals
- **Just transition** — workers, regions, and institutions through structural change

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
- Predominantly **first-party research articles** from the private research pipeline, plus handwritten seeds and approved supplements — all with **committee review** before inclusion
- Full dataset: [`sustainai-global/ethos-training-data-v1`](https://huggingface.co/datasets/sustainai-global/ethos-training-data-v1) on Hugging Face
- Representative samples only in [data/sample/](data/sample/README.md)

See [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) for philosophy and governance.

---

## Development environment (public)

- **Alignment and iteration** on local **solar-powered** development hardware where feasible
- **GPU training** requires additional renewable capacity; we are **seeking funding and partners** for renewable GPU hours rather than defaulting to unconstrained fossil-grid burst training

We do not publish cloud provider accounts, internal hostnames, cost projections, or operational runbooks in this repo.

---

## What we intentionally omit here

The following stay in private development environments:

- Full training scripts, hyperparameter sweeps, and provider-specific runbooks
- Raw or pre-committee datasets
- Production API keys, secrets, and infra-as-code
- Model checkpoint distribution beyond private Hugging Face storage
- Experiment logs and internal evaluation dashboards
- Specific base model sizes, hosting vendors, and training platform choices

---

## Related documentation

- [README.md](README.md) — Repository overview
- [CHARTER.md](CHARTER.md) — Ten Principles of Ethical Intelligence
- [USAGE.md](USAGE.md) — Access policy
- [MODEL_CARD.md](MODEL_CARD.md) — Model card
- [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) — Training principles
- [config/README.md](config/README.md) — Skeleton config placeholders
- [data/sample/README.md](data/sample/README.md) — Sample data plan

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
