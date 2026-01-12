# Agent Guidelines

This document describes how AI agents should work within this repository. Agent-specific files (like `CLAUDE.md`) should reference this document and add any agent-specific instructions.

## Core Principles

1. **Git is the complete record** - All project knowledge, decisions, and history should be captured in the repository. Do not rely on external systems for project state.

2. **Work incrementally** - Commit often with well-structured messages. Each commit should describe what changed and why.

3. **Keep documentation current** - When making changes that affect architecture or design, update the relevant documents in `docs/designs/`.

## Workflow

### Branching

Use feature branches for all work. Branch naming conventions:

- `feature/<description>` - New functionality
- `fix/<description>` - Bug fixes
- `docs/<description>` - Documentation-only changes

Note: Feature and fix branches may include documentation updates; use `docs/` prefix only for documentation-only work.

### Commits

Commit messages should be well-structured and describe:
- **What** the change is
- **Why** it was made

Commit frequently. Before merging to main, rebase to create a clean history.

### Merging

Rebase your feature branch onto main before merging to maintain a linear history.

## Development Process

### Starting Work

Most work begins with an RFC (Request for Comments):

1. Create a draft RFC in `docs/rfcs/`
2. Iterate on the design with stakeholders
3. Once approved, the RFC status changes to `accepted`
4. Implement the accepted design
5. Record key decisions in `docs/adrs/`

For smaller changes that don't require an RFC, ensure the change is still documented appropriately.

### Before Committing

1. Run available tests (`./scripts/project test`)
2. Verify the change works as expected
3. Update relevant documentation in `docs/designs/`

### Verification

All proposed designs should include a verification plan. When implementing:
- Follow the verification plan from the RFC
- Document any deviations or additional verification performed
- Ensure tests cover the new functionality

## Restrictions

### Dependencies

**Agents must not add dependencies without human approval.**

Dependencies include:
- Code libraries and packages
- Frameworks
- External services

Before proposing a new dependency:
1. Document the need and alternatives considered
2. Get explicit human approval
3. Update `docs/designs/dependencies.md` with the approved dependency

If a dependency is already listed in `docs/designs/dependencies.md`, it is pre-approved for use.

## Repository Structure

```
├── AGENTS.md              # This file - general agent instructions
├── CLAUDE.md              # Claude-specific instructions
├── README.md              # Project overview
├── docs/
│   ├── rfcs/              # Request for Comments - design proposals
│   ├── designs/           # Living documentation of current architecture
│   │   ├── architecture.md
│   │   └── dependencies.md
│   └── adrs/              # Architecture Decision Records
└── scripts/               # Development and build scripts
```

## Documentation

### RFCs (`docs/rfcs/`)

RFCs are design proposals with a defined lifecycle:
- **draft** - Under development, not ready for review
- **considering** - Ready for review and discussion
- **accepted** - Approved for implementation
- **rejected** - Not approved (kept for historical record)
- **paused** - Temporarily on hold
- **superseded** - Replaced by a newer RFC

See `docs/rfcs/README.md` for the RFC process and template.

### Design Documents (`docs/designs/`)

Living documents describing current architecture and implementation. These should be kept up-to-date as the system evolves.

Standard documents:
- `architecture.md` - System architecture overview
- `dependencies.md` - Approved dependencies and rationale

### ADRs (`docs/adrs/`)

Architecture Decision Records capture significant technical decisions. When an RFC is accepted, key decisions should be recorded as ADRs.

See `docs/adrs/README.md` for the ADR format.

### Scripts (`scripts/`)

Scripts for common development tasks. See `scripts/README.md` for conventions.
