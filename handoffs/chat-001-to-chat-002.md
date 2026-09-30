# Future Handoff Protocol

This file describes how `chat-001` can hand context to a future `chat-002`. It does not assert that `chat-002` exists.

## Context packet

```text
STATE.md
→ DECISIONS.md
→ OPEN_QUESTIONS.md
→ chats/chat-001/HANDOFF.md
→ relevant architecture/facts
→ exact source evidence
```

## Required checks

- verify temporal cutoff;
- confirm no newer decision supersedes an older one;
- distinguish source fact from project proposal;
- do not load the full transcript unless necessary;
- preserve all RAW files unchanged.

## Suggested first task

Convert the chosen module order into the first project-level specification and MVP backlog, while preserving the M12 boundary and security/read-only constraints.
