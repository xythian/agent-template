# Project Name

<!--
TEMPLATE INSTRUCTIONS (delete this block when customizing):
This README serves as both documentation for the agent-template repository
and as a template for projects created from it. Replace the content below
with your project-specific information.

When creating a new project from this template:
- Update LICENSE.md for your project's licensing terms
- Update .gitignore for your project's language/framework (the template includes common IDE ignores)
-->

Brief description of what this project does and why it exists.

## Getting Started

### Prerequisites

List any prerequisites needed to work with this project.

### Setup

```bash
# Clone the repository
git clone <repository-url>
cd <project-name>

# Run setup script if available
./scripts/setup
```

## Development

### Workflow

This project uses a feature branch workflow:

1. Create a branch from `main`:
   - `feature/<description>` for new functionality
   - `fix/<description>` for bug fixes
   - `docs/<description>` for documentation-only changes

2. Make changes, committing frequently with descriptive messages

3. Before merging, rebase onto `main` for a clean history

4. Merge to `main`

### Common Scripts

```bash
./scripts/setup    # Set up local development environment
./scripts/build    # Build the project
./scripts/test     # Run the test suite
./scripts/lint     # Run linters and formatters
./scripts/clean    # Remove build artifacts
```

### Project Development Script

If the project has local services (databases, queues, etc.), use the project script:

```bash
./scripts/project build   # Build for local development
./scripts/project start   # Start local development services
./scripts/project stop    # Stop local development services
```

## Documentation

- **[Architecture](docs/designs/architecture.md)** - System architecture overview
- **[Dependencies](docs/designs/dependencies.md)** - Approved dependencies
- **[RFCs](docs/rfcs/)** - Design proposals and their status
- **[ADRs](docs/adrs/)** - Architecture decision records

## For AI Agents

See `AGENTS.md` for guidelines on how AI agents should work within this repository.

Agent-specific instructions:
- [Claude](CLAUDE.md)
- [Gemini](GEMINI.md)
- [Codex](CODEX.md)

## Repository Structure

```
├── AGENTS.md              # General AI agent guidelines
├── CLAUDE.md              # Claude-specific instructions
├── GEMINI.md              # Gemini-specific instructions
├── CODEX.md               # Codex-specific instructions
├── README.md              # This file
├── docs/
│   ├── rfcs/              # Design proposals
│   │   ├── README.md      # RFC process documentation
│   │   └── _template.md   # RFC template
│   ├── designs/           # Living architecture documentation
│   │   ├── README.md      # Design docs conventions
│   │   ├── architecture.md
│   │   └── dependencies.md
│   └── adrs/              # Architecture Decision Records
│       ├── README.md      # ADR process documentation
│       └── _template.md   # ADR template
└── scripts/               # Development scripts
    └── README.md          # Script conventions
```

## License

<!--
TEMPLATE NOTE: This template is licensed under Apache 2.0. When using this
template for your own project, update LICENSE.md to reflect your project's
licensing terms.
-->

This project is licensed under the Apache License, Version 2.0. See [LICENSE.md](LICENSE.md) for details.
