# BlueLotus V3 — Deterministic Era (June 2026)

**Status:** Production reference  
**Execution:** `CIO_ONLY_MANUAL` · order routing disabled  
**Production path:** Deterministic Chief Clerk (Zone A) — **no LLM agent council**

---

## What changed

In June 2026 BlueLotus V3 completed a deliberate architectural transition:

| Before | After |
|--------|--------|
| 9-agent Qwen council in pipeline | **Deterministic clerk** — pure Python, no GPU inference |
| Stochastic LLM briefings | **Contradiction map** from governance + portfolio math |
| `run_v3_grand_cycle` in active path | **Quarantined** — manual-only legacy |
| GitHub publish + Telegram in loop | **Optional** — stripped from research pip package |

---

## Why we removed agents from production

This was not nostalgia for simpler code. It was **field evaluation under live operating conditions**.

### 1. Temporal blindness is disqualifying

Frontier LLMs treated stale and fresh signals with equal weight. In a live intelligence package, that corrupts forward probability trees — not a prompt bug, an architectural limit. A clerk who cannot distinguish yesterday's headline from this morning's has no place in capital operations.

See: [Captain's Log — AI Field Evaluation](https://sohweekian.github.io/bluelotus/cio-letter.html) (Edition 047) and `CAPTAINS_LOG_20260622_AI_Field_Evaluation.md` in bluelotus-research.

### 2. Partial reading + confident hallucination

When given multi-file intelligence packages (JSON + TXT + XLSX + DOCX), agents skimmed, then **fabricated** missing sections with full confidence. That is worse than no clerk — it is active disinformation risk.

### 3. Non-reproducible production truth

The holy-grail production loop requires: **same inputs → same analytical outputs → auditable artifacts**. LLM councils violate that contract. Deterministic clerk satisfies it.

### 4. Safety doctrine alignment

`BLV3-DOCTRINE-001` through `007` require manual execution, no order generation, governance before publish. Zone A clerk enforces these from **governance gate + operator verdicts + portfolio integrity** — not from model politeness.

---

## What production runs now

```text
run_v3_pipeline.bat
  → orchestration.run_v3_intelligence_pipeline [--loop]
      → ingest + export + governance gates
      → research_report_generator (deterministic render)
      → orchestration.run_deterministic_clerk_cycle   ← Zone A
      → NITE-PEI + SLICDO learning
      → bluelotus_publisher (dashboard only — optional in research edition)
```

**Legacy council:** `run_v3_grand_cycle.bat` — quarantined, not in `v3_pipeline.yaml`.

---

## Verification (June 2026)

| Gate | Result |
|------|--------|
| `pytest tests/` | 509 passed |
| Report regression audit | 10/10 PASS |
| Production clerk | Deterministic · no LLM |
| P/L integrity | Broker-reported authoritative |

---

## Public research distribution

| Repo | Purpose |
|------|---------|
| [bluelotus-engine](https://github.com/sohweekian/bluelotus-engine) | `pip install bluelotus-engine` — sanitized engine, no publish, no telegram |
| [bluelotus-engine-docs](https://github.com/sohweekian/bluelotus-engine-docs) | Narrative + architecture story |
| [bluelotus-research](https://github.com/sohweekian/bluelotus-research) | Academic theses & doctrines |
| [bluelotus](https://github.com/sohweekian/bluelotus) | Live dashboard (publish surface) |

---

*BlueLotus V3 · The pipeline calculates. The clerk maps contradictions. The CIO decides.*
