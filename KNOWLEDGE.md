# Knowledge Base

## 1. Target product

A conversational, reflective SRE/DevOps agent should operate as an evidence-driven incident workflow rather than a generic chatbot. The core loop is:

`incident → triage → evidence → hypothesis → verification → remediation proposal → approval → execution → recovery verification → resolution → postmortem`

## 2. Runtime state versus long-term memory

LangGraph's current persistence documentation distinguishes thread-scoped checkpoints from cross-thread stores. This maps naturally to:

- current incident execution state;
- long-term incident history/runbooks/knowledge.

The external Chat 1 repository is a third, separate memory layer for research continuity. [R03]

## 3. Operational evidence

Prometheus/Alertmanager provide alert and metric evidence; Loki provides log querying; GitHub provides deployment/change evidence; OpenTelemetry provides service/agent telemetry. The target should correlate these sources rather than treat any single source as authoritative root-cause truth. [R05][R06][R11][R13]

## 4. Safety

The most important security risks around an incident-response agent include prompt injection, sensitive information disclosure, improper output handling and excessive agency. Production mutation should therefore be mediated by policy and approval boundaries. [R09]

## 5. Recovery

Recovery automation should be tested, observable, reproducible and stoppable. Low-risk automated recovery can be staged, while high-impact actions should remain gated until confidence and controls are demonstrated. [R07]

## 6. Documentation

M5 makes repository documentation a first-class context source. Architecture decisions, API contracts, runbooks and operational procedures should live with code and be validated in CI where practical.

## 7. SDD

M2 positions the specification as the contract between product intent and implementation. The project should not ask a coding agent to implement a large epic without the capability-level spec and acceptance evidence.

## 8. Testing

M7 provides unit/TDD discipline; M11 provides integration/E2E/BDD system QA. For agent systems, tests must cover both conventional software behavior and agent behavior, including tool selection, approval gates and evidence grounding.

## 9. Data

PostgreSQL is a strong fit for durable incident records, audit data and relational joins. pgvector can consolidate semantic retrieval with that data when retrieval needs justify it. [R19]

## 10. Agentic development

M1 + M3 supply the harness and context model. OpenAI's Feb 2026 harness-engineering article describes repository knowledge as system of record and emphasizes engineering the environment around the model. [R01]

## 11. Temporal integrity

The supplied M12 document contains some release information published after the executable prompt's Sep 11 cutoff. Those values are retained as source statements but not promoted to cutoff-current state.

## Chat 2 Derived Knowledge — M1 Foundation

### Practical interpretation

M1 is not a product-architecture module. It is a foundation for how the engineering team will use AI while building the product. Its practical output is an operating method: characterize the task, select the tool category and work mode, curate persistent and operational context, write concise outcome-oriented prompts with explicit success criteria, select a coding execution pattern, and review the result with observable validation.

### Seven professional work units

The stable decomposition derived from the complete M1 source is:

1. Task characterization and three-pillar operating model.
2. Tool-category selection and evaluation.
3. Persistent context architecture and `AGENTS.md` baseline.
4. Operational context engineering and context-rot management.
5. Fundamental technical prompting.
6. Coding execution patterns and review loops.
7. Integrated application to M1 canonical cases A–E.

The seven-unit count is a consequence of functional grouping, not a target chosen before source analysis.

### Application boundary

M1 can create or prepare project-facing operating artifacts such as AI-engineering rules, context conventions, prompt contracts, tool-selection criteria and execution/review procedures. It does not by itself justify implementation of FastAPI, LangGraph, RAG, databases, UI, observability, deployment or production incident actions.

### Context boundary for the target project

The SRE reference is used to make M1 concrete: tool decisions should distinguish investigation from consequential mutation; context should prioritize incident evidence, repository conventions, current state and relevant runbooks; prompts should optimize for outcomes and evidence; execution patterns should preserve human review and validation. These are application constraints derived from M1 plus the project reference, not a claim that M1 teaches the SRE domain itself.

### No new project decision

Chat 2 produced no new substantive project decision. It preserved DEC-0001 through DEC-0006 and produced a derived M1 plan only.

## 12. Aplicación de M1 en Chat 2

M1 funciona como fundamento del modo en que se construirá el producto con IA. Las siete unidades son: caracterización de tarea/modo de trabajo; selección y evaluación de herramienta; arquitectura de contexto persistente; gestión operativa del contexto; prompting fundamental; patrones de ejecución de coding; e integración mediante los casos A–E.

La planificación separa contexto persistente, contexto operativo y prompt de tarea; además separa prompting fundamental de patrones de ejecución. M1 se aplica dentro de cada unidad y no mediante un paso final de consolidación.

La trazabilidad completa está en `knowledge/architecture/10-traceability.md` y el plan ejecutable en `knowledge/architecture/11-m1-construction-plan.md`.
