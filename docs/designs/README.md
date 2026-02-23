# Design Documents

This folder contains living documentation of the current architecture and implementation. Unlike RFCs (which capture proposals) or framing documents (which capture product-level design and requirements), design documents describe **how the system currently works**.

## Keeping Documents Current

Design documents must be kept up-to-date as the system evolves. When making changes:

1. Update relevant design documents as part of the same branch
2. Review design docs during code review
3. If a design doc becomes significantly out of date, prioritize updating it

## Standard Documents

These documents should exist in every project:

- **`architecture.md`** - High-level system architecture overview
- **`dependencies.md`** - Approved dependencies and rationale

## Adding New Documents

Create new design documents for significant subsystems or cross-cutting concerns. Use lowercase with hyphens for naming: `feature-name.md`

Examples:
- `authentication.md`
- `data-model.md`
- `api-design.md`

## Document Structure

Design documents are freeform but should typically include:

- Overview of what the component/system does
- Key concepts and terminology
- How it works (architecture, data flow, etc.)
- Important interfaces or APIs
- Operational considerations (if applicable)

Keep documents focused and scannable. Link to code where appropriate rather than duplicating implementation details.
