# Flexiqueue Resources

## Knowledge

### Primary Sources (the codebase itself)
- **`routes/web.php`** — 595-line route definition with inline architectural commentary (spec references, permission middleware, grouped prefixes). The single best entry point for understanding the system's surface area.
- **`routes/api.php`** — Edge device API: pairing, heartbeat, sync, session lifecycle. Shows the edge/central boundary.
- **`app/Models/`** — 40+ models. Key ones: `Program`, `Station`, `Token`, `Session`, `Process`, `ServiceTrack`, `EdgeDevice`, `TransactionLog`.
- **`app/Services/`** — 50+ service classes. Key: `FlowEngine`, `SessionService`, `StationQueueService`, `EdgeModeService`, `EdgePairingService`, `ProgramService`, `TokenService`.
- **`app/Http/Controllers/`** — Controllers by area: `Admin/`, `Api/`, `Auth/`, `Edge/`, plus page controllers (`DisplayController`, `StationPageController`, `TriagePageController`).
- **`resources/js/Pages/`** — Svelte 5 page components organized by domain: `Admin/`, `Display/`, `Edge/`, `Kiosk/`, `Staff/`, `Station/`, `Triage/`.
- **`database/migrations/`** — Full schema evolution from v1 tables to v2 refinements. Shows how the data model grew.

### Documentation
- **`GEMINI.md`** — 14KB AI-assisted documentation dump. Contains spec references, design decisions, and edge case handling.
- **`docs/` directory** — Formal documentation including deployment, beginner guide, and planning docs.
- **`flexiqueue_pitch.md`** and **`flexiqueue_defense_guide.md`** — Capstone defense materials explaining the "why" and high-level architecture.

### External Patterns
- **Laravel Reverb** — First-party Laravel WebSocket server. https://reverb.laravel.com/ . Used for LAN-local realtime without internet dependency.
- **Spatie Laravel Permission** — RBAC package. https://spatie.be/docs/laravel-permission . Flexiqueue uses a custom RBAC sync layer (`SpatieRbacSyncService`).
- **Laravel Inertia v2 + Svelte 5** — Stack matches SecureCAT-v2 exactly. Look at how Flexiqueue structures Inertia page props and shared data.

## Wisdom (Communities)
- **Laravel Discord / Reverb channel** — For WebSocket/Realtime architecture questions.
- **BSIT capstone cohort (Christine, Jaypee)** — Discuss architectural trade-offs in the context of SecureCAT-v2 requirements.
- **Sir Zeus** — Adviser feedback on architectural decisions and scope.

## Gaps
- No formal ADRs (Architecture Decision Records). Architectural knowledge is scattered across `GEMINI.md`, route comments, and service classes. This teaching workspace will bridge that gap.
- No single document explaining the FlowEngine's state machine design — must be reverse-engineered from code.
