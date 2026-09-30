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

# CHAT 2 — CONTENIDO NUEVO

## New consolidated knowledge

Chat2 operationalized M1 as the first AI-engineering foundation for the SRE target. The useful M1 knowledge is represented by the seven canonical steps in `chats/chat-002/M1_PLAN.md`. The plan distinguishes source facts, inherited decisions, proposals and future execution.

## M1 practical rules derived from source

1. Tool choice and mode are explicit decisions, not defaults.
2. Context is a managed engineering resource; use minimum-sufficient selection and isolation.
3. Prompts are contracts with observable success criteria.
4. Workflows use plan/execute/test/review/refactor loops.
5. Repository-local knowledge should be structured for progressive disclosure.
6. Validation and feedback are part of the operating method, not only a final step.
7. M1 does not implement product runtime components.

## Temporal/provenance note

OpenAI Harness Engineering (2026-02-11) corroborates the repository-knowledge/system-of-record and progressive-disclosure approach. It is within the mandatory cutoff.
