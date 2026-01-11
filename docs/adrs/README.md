# Architecture Decision Records (ADRs)

ADRs capture significant technical decisions made during the project. They provide context for future developers (human or AI) about why things are the way they are.

## What is an ADR?

An Architecture Decision Record documents a single decision, including:
- The context that led to the decision
- The decision itself
- The consequences (positive and negative)

## When to Write an ADR

Write an ADR when:
- Making a significant technical choice
- Choosing between multiple valid approaches
- An RFC is accepted (capture key decisions from the RFC)
- Changing a previous decision (supersede the old ADR)

Don't write an ADR for:
- Obvious or trivial decisions
- Decisions that are easily reversible
- Implementation details that don't affect architecture

## ADR Format

We use a format based on Michael Nygard's ADR template:

1. **Title** - Short noun phrase describing the decision
2. **Status** - proposed, accepted, deprecated, superseded
3. **Context** - What is the issue motivating this decision?
4. **Decision** - What is the change we're making?
5. **Consequences** - What are the results of this decision?

See `_template.md` for the full template.

## File Naming

Use sequential numbering with a short description:
- `001-use-postgresql.md`
- `002-api-versioning-strategy.md`
- `003-authentication-approach.md`

## ADR Lifecycle

- **proposed** - Decision is under discussion
- **accepted** - Decision has been agreed upon
- **deprecated** - Decision is no longer relevant
- **superseded** - Replaced by a newer decision (link to the new ADR)

## Index

<!-- Keep an index of ADRs here for easy reference -->

| Number | Title | Status |
|--------|-------|--------|
| 001 | [Example Decision](001-example.md) | accepted |
