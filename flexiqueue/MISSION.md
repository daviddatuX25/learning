# Mission: Flexiqueue Architecture for SecureCAT-v2 Design Decisions

## Why
David is building SecureCAT-v2 — a Laravel 12/Inertia v2/Svelte 5/Tailwind 4 capstone with AI scheduling, OMR, ML triage, and an AI companion. Flexiqueue is the closest real-world full-stack reference project available: same Laravel+Svelte stack, WebSockets, multi-surface orchestration, offline-first architecture, ML integration, and IoT/hardware deployment. By reverse-engineering Flexiqueue's architecture from ground zero, David will internalize patterns he can directly apply to SecureCAT-v2 — avoiding architectural mistakes and making informed trade-off decisions.

## Success looks like
- David can explain Flexiqueue's full architecture stack (routes → controllers → services → models → frontend → realtime → deployment) without looking at the code
- David can identify which of Flexiqueue's patterns apply to SecureCAT-v2 and which don't, with rationale
- David can make an informed decision on SecureCAT-v2's service layer architecture, WebSocket strategy, ML sidecar integration, and offline resilience approach based on Flexiqueue lessons learned
- David can defend architectural choices for SecureCAT-v2 in proposal defense, citing Flexiqueue as a reference

## Constraints
- Project is in active use; code may have been written by multiple authors with varying conventions
- Learning should be driven by exploration of the actual codebase — not abstract theory
- Focus on transferable patterns, not memorizing Flexiqueue-specific implementation details
- Keep lessons grounded in what David can verify by reading the files himself

## Out of scope
- Deep-dive into Svelte 5 or Tailwind 4 syntax (David already knows these from SecureCAT-v2)
- Laravel fundamentals (David already ships Laravel code)
- Re-implementing Flexiqueue features in SecureCAT-v2
- Hardware/IoT details of Orange Pi deployment (unless directly relevant to architectural patterns)
