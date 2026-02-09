<!--
Sync Impact Report:
- Version change: N/A -> 1.0.0
- Modified principles: None (new constitution)
- Added sections: All core principles and governance
- Removed sections: None
- Templates requiring updates: ✅ All updated
- Follow-up TODOs: None
-->

# Phase II – Todo Full-Stack Web Application Constitution

## Core Principles

### I. Spec-Driven Development (NON-NEGOTIABLE)
All implementation must strictly follow written specifications; No feature may be developed without prior specification; All code changes must be traced back to a spec requirement.
<!-- Reasoning: Ensures deterministic behavior, enables reviewability, and maintains project coherence across the team -->

### II. Zero Manual Coding Policy
All code changes must occur exclusively through Claude Code prompts; No direct code editing or manual implementation allowed; All implementation must be reproducible via prompts.
<!-- Reasoning: Maintains process integrity, enables auditability, and ensures all changes follow the spec-driven approach -->

### III. Full-Stack Coherence
Frontend, backend, and database contracts must remain perfectly consistent across all specs; API request/response shapes must match frontend expectations exactly; Database schema must align with API models and UI data usage.
<!-- Reasoning: Prevents integration mismatches, ensures seamless data flow, and maintains system reliability -->

### IV. Security-First Design
All data must be properly isolated between users; JWT authentication must be stateless with signature verification on every request; User ownership must be enforced on all data operations.
<!-- Reasoning: Protects user data, prevents unauthorized access, and maintains trust in the application -->

### V. Deterministic Behavior
Same inputs must always produce identical outputs; System behavior must be predictable and repeatable; All operations must be idempotent where possible.
<!-- Reasoning: Ensures reliability, simplifies debugging, and enables proper testing -->

### VI. Technology Stack Compliance
Must use the fixed technology stack: Next.js 16+ (App Router, TypeScript) for frontend; FastAPI (Python) for backend; SQLModel for ORM; Neon Serverless PostgreSQL for database; Better Auth with JWT for authentication.
<!-- Reasoning: Ensures consistency, reduces complexity, and maintains compatibility across the project -->

## Development Standards

### API and Architecture Requirements
All API routes must live under `/api/`; All authenticated requests must require a valid JWT token; Proper HTTP status codes must be used consistently (200, 201, 400, 401, 404, 500); All API behavior must follow REST conventions.
<!-- Reasoning: Maintains architectural consistency, ensures proper authentication, and follows industry standards -->

### Frontend Standards
Frontend must be responsive with clear loading and empty states; Frontend must consume backend only via defined API client; All API calls must include Authorization header; No direct database or auth logic in frontend.
<!-- Reasoning: Ensures good user experience, maintains separation of concerns, and enforces proper security -->

### Quality Requirements
Backend must implement proper input validation via Pydantic; Database access must only occur through SQLModel; JWT token expiry must be enforced; User_id in token must match route user_id for all operations.
<!-- Reasoning: Ensures data integrity, prevents security vulnerabilities, and maintains system reliability -->

## Spec Integrity Rules

### Specification Governance
Specifications are the ultimate source of truth for all development; If implementation conflicts with spec, the spec must be updated first; Cross-spec dependencies must be explicit and documented; No feature may span multiple specs without proper references.
<!-- Reasoning: Maintains consistency between design and implementation, prevents drift, and ensures traceability -->

### Change Management
All changes in one layer must be reflected across all affected specifications; Every feature must be defined in a spec before implementation begins; Claude Code must reference specs using @specs/... paths.
<!-- Reasoning: Ensures full-stack coherence, prevents inconsistencies, and maintains the spec-driven approach -->

## Governance

This constitution supersedes all other development practices and guidelines; All amendments must be documented, approved, and implemented with proper migration plans; All code reviews and PR approvals must verify compliance with these principles; Every commit must be reviewable via specs, prompts, and commit history.
<!-- Reasoning: Establishes authority of these principles, ensures consistent enforcement, and maintains project integrity -->

**Version**: 1.0.0 | **Ratified**: 2026-02-05 | **Last Amended**: 2026-02-05
