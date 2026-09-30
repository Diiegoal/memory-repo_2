# Module Coverage Audit

| Module | Real content focus | Role in build | Coverage of target |
|---|---|---|---|
| M1 | Tool/context/prompt foundations | Foundation | Strong for AI-assisted workflow; indirect for SRE domain |
| M2 | SDD/OpenSpec | Specification gate | Strong for agentic contract discipline |
| M3 | Copilot harness/EPE/subagents/hooks/MCP | Agentic operating system | Strong for AI-native execution method |
| M4 | Planning/backlog/AC/DoD/continuous plan | Product discovery and planning | Strong for scope/acceptance; incident domain must be supplied by project |
| M5 | ADR/C4/API/docs-as-code | Architecture and knowledge | Strong for durable agent/human context |
| M6 | Security/privacy/regulation/LLM security | Security-by-design | Strong principles; executor details require project work |
| M7 | TDD/unit quality/AI test generation | Unit quality | Strong generic testing, partial Python fit |
| M8 | Postgres/SQL/indexes/pgvector/AI DB tooling | Data foundation | Strong |
| M9 | Backend architecture/refactoring/ticket-to-PR | Backend | Partial exact fit because examples are Node/TS |
| M10 | React/frontend/design-to-code | Operator UI | Partial because target MVP may use Streamlit; principles transfer |
| M11 | Integration/E2E/BDD/AI QA | System QA | Strong conceptually; exact SRE scenarios must be authored |
| M12 | RAG + SRE incident reference | Reference only | Direct target architecture source; excluded from build |
| M13 | PR review/IaC/CI/CD/DevSecOps | Delivery/operations | Strong delivery foundation; SRE runtime depth still requires project work |

## Coverage classifications

- **COVERED:** core capability is materially taught.
- **COVERED INDIRECTLY:** transferable patterns exist, but exact target implementation differs.
- **PARTIALLY COVERED:** only a significant subset is taught.
- **COVERED BUT INSUFFICIENT FOR PRODUCT:** concept exists but target-specific depth is missing.
- **NOT COVERED:** no material curriculum evidence found in the audited modules.

## Target-specific gaps

1. FastAPI/Python production implementation is not fully covered by the backend module.
2. LangGraph incident orchestration and SRE-specific tool design are reference-driven rather than taught as a dedicated construction module.
3. Exact SLO/SLI/error-budget/on-call practices need a project-specific SRE layer.
4. Incident-specific synthetic datasets/evals need to be authored.
5. Secure executor isolation and credential separation need dedicated implementation work.
6. Slack event and approval mechanics need an integration lab.
7. Runtime agent memory policy needs an explicit retention/provenance design.

---

# CHAT 2 — CONTENIDO NUEVO

## M1 coverage

The practical M1 inventory is represented by seven stable functional units in `chats/chat-002/M1_PLAN.md`. Each unit has 26 fields. P04 explicitly covers context rot and W/S/C/I; P06 explicitly covers the five coding patterns; P07 explicitly covers A–E.

# CHAT 2 — CUMULATIVE UPDATE

## Current repository verification
Chat2 re-queried `Diiegoal/CursoIA` on `main` and retrieved all 68 Markdown files across the 13 module directories. The current M1 directory contains exactly five Markdown files with current Git blob identifiers. No module name was silently corrected.

## M1 step mapping
The five M1 source files map to seven stable work units. P04 owns context rot plus Write/Select/Compress/Isolate. P06 owns all five coding patterns. P07 owns cases A–E and the integrated evidence chain.

