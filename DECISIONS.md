# Decisions

## Active decisions

### DEC-0001 — Professional module order
Status: accepted

Adopt `M1 → M3 → M4 → M2 → M6 → M5 → M7 → M8 → M9 → M10 → M11 → M13`.

### DEC-0002 — Exclude M12 from the Agentic SDLC
Status: accepted

Use M12 only as a knowledge/reference source for the SRE/DevOps target. Do not place it in the 12-module order or treat it as a construction stage.

### DEC-0003 — Security and documentation as gates plus loops
Status: accepted

M6 provides the security/privacy gate before architecture is fixed; M5 turns those decisions into living architecture/knowledge. Both recur throughout development.

### DEC-0004 — Read-only-first agent
Status: accepted

The initial agent investigates and proposes remediation but does not mutate production. Consequential actions require policy checks, human approval and a separated executor.

### DEC-0005 — Postgres-first retrieval consolidation
Status: accepted

Use PostgreSQL as authoritative operational storage and evaluate pgvector as the first semantic retrieval option before adding a separate vector database.

### DEC-0006 — Streamlit is optional at product level
Status: accepted

Use Streamlit as a practical first operator UI/demo, but keep the underlying product architecture independent of it. Slack can serve as an operational interaction surface.

## Decision principles

- Decisions describe what Chat 1 adopted; recommendations remain distinguishable in knowledge documents.
- Changes require a new decision record and temporal context.

---

# CHAT 2 — CONTENIDO NUEVO

## Chat 2 review

### New substantive decisions

**0** — No new substantive decision was adopted during Chat 2.

Chat 2 confirmed the applicability of DEC-0001 through DEC-0006 but did not create a new decision record.
