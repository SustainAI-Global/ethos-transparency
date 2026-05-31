# Model Card — Ethos-32B (ESI)

A **public philosophy** model card for transparency. This is not a weights card — checkpoints are private and hosted only. Numeric evaluation results will be added when our methodology is published.

Repository home: [README.md](README.md) · SustainAI: [sustainai.global](https://sustainai.global/)

---

## Model summary

| Field | Value |
|-------|--------|
| **Model name** | Ethos-32B (ESI — Ethical Specialized Intelligence) |
| **Organization** | [SustainAI Global](https://sustainai.global/) (Texas nonprofit, 501(c)(3) pending) |
| **Version** | v1 (private beta) |
| **Base model** | [Qwen/Qwen3-32B-FP8](https://huggingface.co/Qwen/Qwen3-32B-FP8) |
| **Base license** | Apache 2.0 (base only; Ethos adaptations are not redistributed as weights) |
| **Fine-tuning** | QLoRA supervised fine-tuning on domain-aligned instruction data |
| **Access** | Hosted chat + API only — see [USAGE.md](USAGE.md) |

---

## Intended use

Ethos-32B is intended to support **reasoning and explanation** in:

- **Sustainable economics** — systems, incentives, and job-aware growth
- **Renewable energy** — transition pathways, deployment tradeoffs, grid concepts
- **Green finance** — risk framing, disclosure themes, capital alignment (not personalized investment advice)
- **Ethical AI** — humility, deferral, and human-centered deployment
- **Job creation and just transition** — workforce and regional impacts of structural change

### Appropriate users

- Educators, students, and researchers studying green transition topics
- Nonprofit and civic planners exploring scenarios (with human review)
- Mission-aligned businesses under API or chat agreements
- SustainAI program participants via [Green Points](https://sustainai.global/)

### Out-of-scope uses

- Medical, legal, or safety-critical engineering sign-off without licensed professionals
- Autonomous trading or individualized financial product recommendations
- Harassment, deception, environmental greenwashing at scale, or labor exploitation
- Building competing hosted models by extracting or distilling private checkpoints
- Any use violating [USAGE.md](USAGE.md) or signed agreements

---

## Training data philosophy

| Topic | Approach |
|-------|----------|
| **Scale** | Approximately **8k–25k** curated examples — quality over quantity |
| **Composition** | Synthetic generation plus human and **committee review** before acceptance |
| **Transparency** | Full corpus planned as public dataset **`ethos-training-data-v1`** on Hugging Face when published |
| **Samples** | 50–100 representative examples in [data/sample/](data/sample/README.md) when ready |
| **What we avoid** | Scraped noise at web scale, unchecked synthetic dumps, or undisclosed private corpora |

Detailed governance: [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md).

---

## Alignment and behavior design

Ethos is trained and served with explicit themes (see draft outline in [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md)):

- Ethical behavior and refusal of clearly harmful requests
- Care for **humanity**, **Earth**, and **animals**
- **Humility** — acknowledge limits, cite uncertainty, defer to experts when stakes are high
- **Jobs-first** — favor outcomes that sustain meaningful work
- **Systems thinking** — connect economic, energy, and social layers

The **agent layer** reinforces routing and deferral so the core model does not overclaim authority in production chat.

---

## Limitations

- **Not omniscient** — knowledge cutoff and domain gaps apply; verify important facts independently
- **Not a substitute for professionals** — especially law, medicine, engineering, and regulated finance
- **Synthetic data bias** — committee review reduces but does not eliminate systematic errors
- **English-primary v1** — other languages may be weaker unless explicitly evaluated later
- **Hosted-only** — behavior may change as we update weights and safety policies without public checkpoint releases
- **Evaluation incomplete** — public benchmarks and internal rubrics are still being finalized

Users should treat outputs as **decision support**, not authoritative commands.

---

## Humility and deferral

Ethos is designed to:

- State when evidence is insufficient or contested
- Narrow scope when a question exceeds training emphasis
- Recommend human, local, or licensed expert follow-up for high-stakes decisions
- Avoid false precision on forecasts, legal outcomes, or site-specific engineering

This is intentional product design, not an accident of base model behavior.

---

## Environmental alignment

> *We align models with the world we want — including how they are built.*

Development emphasizes **solar-powered local iteration** where feasible and a path to **100% renewable** training and serving by 2030. See [VISION.md](VISION.md) and [ARCHITECTURE.md](ARCHITECTURE.md).

---

## Evaluation results — forthcoming

We are finalizing evaluation methodology aligned with ESI goals (not only generic academic benchmarks). Planned public sections include:

- Domain rubrics (economics, energy, finance, transition)
- Safety and refusal behavior summaries
- Humility / deferral spot checks
- Comparison notes vs. base Qwen3-32B-FP8 (qualitative where appropriate)

**No private evaluation numbers are published in this card.** Results will appear here and on [sustainai.global](https://sustainai.global/) when ready.

---

## Distribution

| Artifact | Public? |
|----------|---------|
| This model card & docs | Yes |
| Training dataset (full) | Planned — Hugging Face `ethos-training-data-v1` |
| Sample rows | Planned — [data/sample/](data/sample/README.md) |
| Model weights | **No** — private HF, hosted inference only |

---

## Related documentation

- [README.md](README.md) — Repository overview
- [ARCHITECTURE.md](ARCHITECTURE.md) — System layers
- [USAGE.md](USAGE.md) — Access policy
- [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) — Training principles
- [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) — System prompt (draft)
- [VISION.md](VISION.md) — Long-term vision

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
