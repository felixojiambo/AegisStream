# AegisStream

**About:** Enterprise workflow platform for structured case triage, knowledge grounding, and human-reviewed operational automation.

---

## Repository Structure

This repository is organized as a monorepo:

- `core-service/` — Spring Boot backend (authentication, workflows, case management, audit)
- `web/` — Next.js frontend (internal operations dashboard)
- `infra/` — Local development tooling (Docker Compose, Postgres, Redis, object storage)
- `docs/` — Architecture documents, ADRs, and phase checklists

---

## Architecture Overview (High Level)

AegisStream is designed as a modular distributed system:

- **Core Service**: System of record, RBAC, workflows, audit logging
- **Runtime Services**: Asynchronous processing and knowledge workflows
- **Web Interface**: Internal operations console
- **Infrastructure Layer**: Local and production environment orchestration

---

## Local Development (To Be Completed in Phase 1)

### Prerequisites
- Java 21+
- Maven or Gradle
- Node.js 18+
- Docker (for local services)

### Planned Local Run Steps
1. Start infrastructure services
2. Run core-service
3. Run web frontend
4. Access dashboard at `http://localhost:3000`

(Detailed steps will be added during Phase 1 setup.)

---

## Development Model

- Trunk-based development
- Short-lived feature branches
- Pull requests required for merge
- CI must pass before merging

---

## License

Apache-2.0 license
