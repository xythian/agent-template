# Scripts

This folder contains scripts for common development tasks. Both humans and AI agents should use these scripts for consistent workflows.

## Conventions

### Naming

Use lowercase names without extensions for maximum portability:
- `setup` - not `setup.sh` or `setup.py`
- `build` - not `build.sh`
- `test` - not `run-tests.sh`

If a script is language-specific, use appropriate extension (`setup.py`, `build.js`).

### Project Script

Projects should provide a `./scripts/project` script as a single entry point for all development tasks. This script should support the following subcommands (when applicable):

| Subcommand | Purpose |
|------------|---------|
| `setup` | Set up local development environment |
| `build` | Build the project |
| `test` | Run the test suite |
| `lint` | Run linters and formatters |
| `clean` | Remove build artifacts |
| `start` | Start local development services (databases, queues, etc.) |
| `stop` | Stop local development services |

Example usage:
```bash
./scripts/project setup   # One-time setup
./scripts/project build   # Build the project
./scripts/project test    # Run tests
./scripts/project start   # Start local services
./scripts/project stop    # Stop local services
```

This pattern provides a single, consistent entry point for both humans and agents.

### Script Requirements

Scripts should:

1. **Be idempotent** - Running multiple times should be safe
2. **Work from any directory** - Use `cd "$(dirname "$0")/.."` pattern to find project root
3. **Exit with appropriate codes** - 0 for success, non-zero for failure
4. **Provide helpful output** - Show what's happening, especially for long-running tasks
5. **Document prerequisites** - Note any required tools or environment setup

### Example Script Structure

```bash
#!/usr/bin/env bash
set -euo pipefail

# Navigate to project root
cd "$(dirname "$0")/.."

echo "Running tests..."
# test commands here

echo "Tests complete."
```

## Adding New Scripts

1. Create the script in this folder
2. Make it executable: `chmod +x scripts/your-script`
3. Add a brief description to this README if it's a commonly-used script
4. Test that it works from both the project root and other directories

## Available Scripts

<!-- List project-specific scripts here as they are added -->

*No project-specific scripts yet.*
