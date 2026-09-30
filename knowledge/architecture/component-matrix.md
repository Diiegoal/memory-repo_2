# Module → Component Matrix

| Product component | Primary modules | Secondary modules | M12 reference contribution |
|---|---|---|---|
| Incident intake | M4, M2, M9 | M5, M11 | alert → incident flow |
| Dedup/correlation | M4, M2, M8, M9 | M7, M11 | fingerprint/dedup concept |
| Incident state | M2, M8, M9 | M7, M11 | LangGraph state machine pattern |
| Evidence tools | M2, M5, M9 | M7, M11, M13 | Prometheus/Loki/GitHub/AWS/K8s examples |
| RAG/runbooks | M5, M8, M9 | M6, M11 | historical incidents/runbooks |
| Human approval | M2, M6, M9, M10 | M11, M13 | HITL/Slack reference |
| Secure executor | M6, M9, M13 | M7, M11 | separate executor reference |
| Recovery verification | M2, M7, M8, M9, M11 | M13 | verify after action |
| Agent observability | M3, M5, M11, M13 | M7 | LangSmith/OTel pattern |
| Postmortem | M5, M8, M9, M11 | M13 | SRE postmortem reference |
