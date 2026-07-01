# 0001: Architectural Map Established

**Status:** active

David started Flexiqueue study with the goal of deep architectural understanding for SecureCAT-v2 design decisions. Lesson 1 (0001-architectural-map.html) established the full-system map: four surfaces, route/permission grouping, service layer composition, FlowEngine state machine, data model, WebSocket dual-driver pattern, Edge/Central architecture, and append-only audit logging.

**Evidence:** David reviewed all key source directories (Models, Services, Controllers, Migrations, Routes) and the capstone defense pitch. He confirmed his mission is architectural insight for SecureCAT-v2, not hands-on Flexiqueue modification.

**Implications:**
- Next lessons should zoom into specific patterns that directly map to SecureCAT-v2 needs: service layer composition, WebSocket broadcasting, permission-route grouping, AI/ML sidecar integration patterns, and Edge device sync.
- David has existing SecureCAT-v2 context (Laravel 12/Inertia/Svelte 5, AI SDK, OMR, ML triage) — Flexiqueue lessons should contrast & compare, not teach from scratch.
- The teaching workspace is at `/home/user/Projects/flexiqueue/teaching-space/`.
