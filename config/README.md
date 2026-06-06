# Training configuration (placeholders)

This directory will hold **skeleton, public-safe** training configuration references for transparency — not executable configs with secrets, API keys, or private paths.

---

## Current status

**No working configs are published yet.**

Planned placeholders (documentation only):

| File (planned) | Purpose |
|----------------|---------|
| `qlora_sft_skeleton.yaml` | High-level QLoRA SFT parameters (ranks, targets) — values TBD |
| `unsloth_notes.md` | Public notes on QLoRA via **Unsloth** — skeleton config forthcoming |
| `phase_manifest.md` | Mapping of training phases to config files — see [ARCHITECTURE.md](../ARCHITECTURE.md) |

---

## What will not appear here

- Live API keys or Hugging Face tokens
- Private cloud instance IDs or internal hostnames
- Copy-paste training commands tied to paid GPU accounts
- Hyperparameter grids from undisclosed experiments

Full training execution remains in the private development repository by invitation.

---

## Public references

- Base model: open-licensed **Qwen3-class** base (Apache 2.0) — specific size documented only in private implementation configs
- Adaptation approach: **QLoRA** fine-tuning (see [ARCHITECTURE.md](../ARCHITECTURE.md))
- Tooling (planned documentation): **Unsloth** — skeleton config forthcoming

---

## Related documentation

- [ARCHITECTURE.md](../ARCHITECTURE.md) — Phased training roadmap
- [CHARTER.md](../CHARTER.md) — Ten Principles of Ethical Intelligence
- [ETHICAL_GUIDELINES.md](../ETHICAL_GUIDELINES.md) — Data and alignment principles
- [README.md](../README.md) — Repository overview

---

## Contact

**[ai@sustainai.global](mailto:ai@sustainai.global)** · [sustainai.global](https://sustainai.global/)
