# Ethos ESI Transparency

**Ethos ESI** (Ethical Specialized Intelligence) is SustainAI Global's specialist AI for sustainable economics, renewable energy, green finance, and a just transition. Its ethical foundation is [The Charter for Beneficial Intelligence](CHARTER.md): ten principles governing how Ethos reasons and serves. This public repository documents **how and why** we build Ethos: methodology, values, architecture, access policy, and transparency artifacts.

**SustainAI Global** is a Texas nonprofit corporation (501(c)(3) pending) dedicated to public-good AI. Learn more at [sustainai.global](https://sustainai.global/).

> **Canonical source:** Technical architecture, training pipelines, and deployment details live in the private [`ethos-esi`](https://github.com/SustainAI-Global/ethos-esi) repo. This repository is a **read-only mirror** of approved public artifacts.

---

## What is Ethos ESI?

Ethos ESI is a fine-tuned specialist built on an **open-licensed Qwen3-class base** (Apache 2.0). It is designed to reason ethically about jobs-first growth, truly green systems, and human–AI partnership — not to replace human judgment in high-stakes decisions.

**v1** includes all three architecture layers: the fine-tuned core model, an agent layer (skills, tools, humility/deferral), and a hosted **Ethos API** plus private-beta chat. API access is available under signed agreements. Application repos (economics, jobs, content tools) live separately and connect via the standard Ethos API.

---

## What is in this repository?

| Area | Description |
|------|-------------|
| [CHARTER.md](CHARTER.md) | The Ten Principles of Ethical Intelligence — core ESI charter |
| [MISSION.md](MISSION.md) | SustainAI nonprofit mission and values |
| [VISION.md](VISION.md) | Long-term vision for ESI and renewable AI |
| [ARCHITECTURE.md](ARCHITECTURE.md) | Public-safe high-level system design |
| [USAGE.md](USAGE.md) | Hosted access policy (chat and API) |
| [MODEL_CARD.md](MODEL_CARD.md) | Public model card (philosophy and intended use) |
| [SYSTEM_PROMPT.md](SYSTEM_PROMPT.md) | Official system prompt (draft placeholder) |
| [ETHICAL_GUIDELINES.md](ETHICAL_GUIDELINES.md) | Training and alignment principles |
| [data/sample/](data/sample/README.md) | Representative sample data (when published) |
| [config/](config/README.md) | Skeleton training config placeholders |

**Not in this repo:** training code, raw datasets, model weights, agent/backend implementation, infrastructure secrets, or provider-specific runbooks. Those remain in separate private repositories by invitation.

---

## Datasets and model weights

| Asset | Status | Access |
|-------|--------|--------|
| Full training dataset (`ethos-training-data-v1`) | [`sustainai-global/ethos-training-data-v1`](https://huggingface.co/datasets/sustainai-global/ethos-training-data-v1) on Hugging Face | Public when published |
| Model weights (`ethos-esi`) | Private Hugging Face — not published | **Hosted only** — no local downloads |
| Sample examples | [data/sample/](data/sample/README.md) | 50–100 representative rows when ready |

Users interact with Ethos through **hosted chat** and **API** only. See [USAGE.md](USAGE.md) for access tiers and agreements.

---

## Related documentation

- [CHARTER.md](CHARTER.md) — Ten Principles of Ethical Intelligence
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

Documentation and transparency artifacts in this repository — including [The Charter for Beneficial Intelligence](CHARTER.md) — are published so the public can see **what we are doing and why**, not as open material for reuse or adaptation.

They are licensed under [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International](LICENSE) (CC BY-NC-ND 4.0), Copyright SustainAI Global. You may read and share with attribution for non-commercial purposes. Commercial use and derivative works require written permission from SustainAI Global.
