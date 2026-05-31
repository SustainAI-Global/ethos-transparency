# Ethos-32B Transparency

**Ethos-32B** is SustainAI Global's **Ethical Specialized Intelligence (ESI)** model — a 32B-parameter language model aligned for sustainable economics, renewable energy, green finance, and a just transition. This public repository documents **how and why** we build Ethos: methodology, values, architecture, access policy, and transparency artifacts.

**SustainAI Global** is a Texas nonprofit corporation (501(c)(3) pending) dedicated to public-good AI. Learn more at [sustainai.global](https://sustainai.global/).

---

## What is Ethos-32B?

Ethos-32B (ESI) is a fine-tuned specialist built on [Qwen/Qwen3-32B-FP8](https://huggingface.co/Qwen/Qwen3-32B-FP8) (Apache 2.0). It is designed to reason ethically about jobs-first growth, truly green systems, and human–AI partnership — not to replace human judgment in high-stakes decisions.

**v1** includes the fine-tuned core model, an agent layer, and private-beta hosted chat. API access is available under signed agreements. Application repos (economics, jobs, content tools) live separately and are not part of this repository.

---

## What is in this repository?

| Area | Description |
|------|-------------|
| [MISSION.md](MISSION.md) | SustainAI nonprofit mission and values |
| [VISION.md](VISION.md) | Long-term vision for ESI and renewable AI |
| [ARCHITECTURE.md](ARCHITECTURE.md) | Public-safe high-level system design |
| [USAGE.md](USAGE.md) | Hosted access policy (chat and API) |
| [MODEL_CARD.md](MODEL_CARD.md) | Public model card (philosophy and intended use) |
| [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) | Official system prompt (draft placeholder) |
| [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) | Training and alignment principles |
| [data/sample/](data/sample/README.md) | Representative sample data (when published) |
| [config/](config/README.md) | Skeleton training config placeholders |

**Not in this repo:** training code, raw datasets, model weights, agent/backend implementation, or infrastructure secrets. Those remain in a separate private development repository by invitation.

---

## Datasets and model weights

| Asset | Status | Access |
|-------|--------|--------|
| Full training dataset (`ethos-training-data-v1`) | Planned on [Hugging Face](https://huggingface.co/) — not published yet | Public when released |
| Model weights (`ethos-32b`) | Private Hugging Face — not published | **Hosted only** — no local downloads |
| Sample examples | [data/sample/](data/sample/README.md) | 50–100 representative rows when ready |

Users interact with Ethos through **hosted chat** and **API** only. See [USAGE.md](USAGE.md) for access tiers and agreements.

---

## Related documentation

- [MISSION.md](MISSION.md) — Why SustainAI exists
- [VISION.md](VISION.md) — Where we are headed
- [ARCHITECTURE.md](ARCHITECTURE.md) — How Ethos is built (high level)
- [USAGE.md](USAGE.md) — How to access Ethos
- [MODEL_CARD.md](MODEL_CARD.md) — Model identity and limitations
- [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) — Alignment and data philosophy
- [CONTRIBUTING.md](CONTRIBUTING.md) — Contributing to transparency docs

---

## Contact

Questions about transparency, documentation, or public collaboration:

**[ai@sustainai.global](mailto:ai@sustainai.global)**

Website: [https://sustainai.global/](https://sustainai.global/)

---

## License

Documentation and transparency artifacts in this repository are released under the [MIT License](LICENSE), Copyright SustainAI Global.
