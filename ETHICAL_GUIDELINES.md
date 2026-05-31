# Ethical Guidelines — Training and alignment

These principles govern how SustainAI Global builds **Ethos-32B (ESI)** and what we publish in this transparency repository. They apply to data, training phases, and hosted access — not to undisclosed private experiments.

[SustainAI Global](https://sustainai.global/) · Contact: **[ai@sustainai.global](mailto:ai@sustainai.global)**

---

## Quality over quantity

We target roughly **8k–25k** high-quality instruction examples, not millions of low-signal rows. Each example should teach **reasoning style** and **domain care**, not trivia volume.

Smaller, reviewed corpora are easier to audit, explain to the public, and improve iteratively than opaque web-scale scrapes.

---

## Committee-reviewed synthetic data

Much of our data is **synthetically generated** then filtered through **human and committee review** before training or public release.

Reviewers check for:

- Factual plausibility and appropriate uncertainty language
- Alignment with jobs-first and truly-green framing
- Absence of harassment, discrimination, or manipulative persuasion
- Consistency with deferral and humility expectations

Examples that fail review are revised or discarded — not silently included.

---

## Public dataset transparency

The full training corpus is planned for public release as **`ethos-training-data-v1`** on [Hugging Face](https://huggingface.co/) when publication criteria are met (committee sign-off, privacy redaction, documentation).

Until then:

- This repo describes **philosophy and methodology** only
- [data/sample/](data/sample/README.md) will hold **50–100 representative** rows — not a stand-in for the full corpus
- We will **not** publish fabricated sample JSONL to simulate completeness

---

## Hosted-only access

Ethical stewardship includes **how** models are deployed:

- Weights stay **private**; users access Ethos via **hosted chat** and **API** under [USAGE.md](USAGE.md)
- We can update safety behavior, monitor misuse, and honor agreements without encouraging unconstrained open-weight proliferation
- For-profit use is limited and contract-governed — not the center of nonprofit mission

---

## Alignment themes in training

Training and system design reinforce:

| Theme | Training intent |
|-------|-----------------|
| Ethical behavior | Refusal and redirection for harmful uses |
| Care for humanity, Earth, animals | Multi-stakeholder reasoning in domain answers |
| Humility | Uncertainty, scope limits, expert deferral |
| Jobs-first | Employment and transition impacts in economic analysis |
| Systems thinking | Link energy, capital, policy, and labor |

The official prompt will be published in [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) before private beta.

---

## Phased honesty

We publish **phases** (SFT → tools → routing → later DPO/ORPO) in [ARCHITECTURE.md](ARCHITECTURE.md) and report evaluation as **forthcoming** in [MODEL_CARD.md](MODEL_CARD.md) rather than inventing metrics.

When results are ready, we will describe methodology before numbers so the community can interpret them.

---

## Environmental integrity

Development prioritizes **renewable-powered** work where feasible and honest disclosure of GPU energy sources as we scale. “Green AI” requires operational truth, not marketing alone — see [VISION.md](VISION.md).

---

## What we do not do

- Train on undisclosed private personal data without legal basis and redaction
- Release unchecked synthetic dumps as “open data”
- Distribute weights publicly while claiming safety cannot be updated
- Use this transparency repo to leak private infra, keys, or raw pre-review datasets

---

## Related documentation

- [README.md](README.md) — Repository overview
- [MISSION.md](MISSION.md) — Nonprofit mission
- [MODEL_CARD.md](MODEL_CARD.md) — Model card
- [ARCHITECTURE.md](ARCHITECTURE.md) — Training phases
- [USAGE.md](USAGE.md) — Access policy
- [data/sample/README.md](data/sample/README.md) — Sample data plan
- [CONTRIBUTING.md](CONTRIBUTING.md) — How to help

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
