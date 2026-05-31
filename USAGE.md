# Usage and access policy

Ethos-32B is **not distributed as downloadable weights**. SustainAI Global hosts the model and controls access through **chat** and **API** surfaces so we can meet nonprofit stewardship, safety, and fairness goals.

Program details and invitations: [sustainai.global](https://sustainai.global/)

---

## Core policy

| Principle | Policy |
|-----------|--------|
| Model weights | **Always private** — stored on private Hugging Face (`ethos-32b`, not public) |
| End-user access | **Hosted chat** and **API only** — no local model downloads |
| Open weights | **Not offered** — users cannot pull checkpoints for self-hosting |
| Transparency | Methodology and data philosophy published here; full dataset on HF when live |

Private weight storage is an **internal artifact** for serving infrastructure. It is not a distribution channel for the public.

---

## Hosted chat (private beta)

**Chat** is the primary way individuals and partners experience Ethos during v1 private beta.

| Aspect | Detail |
|--------|--------|
| Availability | Private beta — by **invitation** |
| How to request access | Through [sustainai.global](https://sustainai.global/) |
| Early access | **Green Points Tier 3+** members receive early **chat** access as tiers are rolled out on the website |
| What you get | Web-based conversation with Ethos-32B via the agent and safety stack |

Chat access does not grant API keys, weight files, or rights to resell model outputs as a hosted service.

---

## API access

**API** access is for organizations and integrators with a formal relationship to SustainAI.

| Aspect | Detail |
|--------|--------|
| Requirement | **Signed agreement or contract** only |
| Use cases | Approved integrations aligned with mission (education, research partners, green enterprise tools, etc.) |
| Self-serve keys | Not available from this repository or public signup |

Contact **[ai@sustainai.global](mailto:ai@sustainai.global)** for API partnership inquiries.

---

## Commercial and for-profit use

SustainAI is a nonprofit; Ethos is **not** designed as a proprietary SaaS rent-extraction product.

- **For-profit access** is possible in limited cases but is **not** our core revenue model
- Pricing, where applicable, reflects **fair market value** and mission fit — not unlimited commercial relicensing of weights
- Redistribution, competitive foundation-model hosting, or fine-tune resale of our private checkpoints is **not** permitted without explicit written terms

---

## What users never receive

- Model weight files (`.safetensors`, GGUF, or equivalent)
- Private Hugging Face credentials or repo access
- Training code, raw datasets, or internal agent/backend source from the private development repo
- Guarantees of uptime or SLAs except as specified in signed agreements

---

## Green Points and community access

The [Green Points](https://sustainai.global/) program on sustainai.global rewards aligned participation. Tier benefits for early chat are described on the website and may evolve; this document only notes that **Tier 3+** is the threshold for early chat access in v1 planning.

---

## v1 product scope

**v1 includes:**

- Fine-tuned Ethos-32B core model (private weights)
- Agent layer for routing and emerging tool use
- Private-beta hosted chat
- API under signed agreements (select partners)

**v1 does not include:**

- Public weight release
- Separate application repos (economics, jobs, content) — those ship elsewhere
- Published evaluation leaderboard in this repo (forthcoming)

---

## Related documentation

- [README.md](README.md) — Repository overview
- [MODEL_CARD.md](MODEL_CARD.md) — Intended use and limitations
- [ARCHITECTURE.md](ARCHITECTURE.md) — Layered system design
- [MISSION.md](MISSION.md) — Nonprofit mission
- [CONTRIBUTING.md](CONTRIBUTING.md) — Contributing to docs

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
