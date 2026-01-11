# RFCs (Requests for Comments)

RFCs are design proposals for significant changes to the project. They provide a structured way to propose, discuss, and document design decisions before implementation.

## When to Write an RFC

Write an RFC when:
- Adding significant new functionality
- Making architectural changes
- Introducing new dependencies
- Changing established patterns or conventions
- Any change that would benefit from upfront design discussion

For small, well-understood changes, an RFC may not be necessary.

## RFC Lifecycle

```
draft → considering → accepted/rejected/paused
                            ↓
                       superseded (if replaced by newer RFC)
```

### Statuses

- **draft** - Under development, not ready for review. Use this while gathering thoughts and fleshing out the proposal.

- **considering** - Ready for review and discussion. Stakeholders should review and provide feedback.

- **accepted** - Approved for implementation. Work can proceed based on this design.

- **rejected** - Not approved. The RFC is kept for historical record, including rationale for rejection.

- **paused** - Temporarily on hold. May be revisited later when circumstances change.

- **superseded** - Replaced by a newer RFC. Link to the superseding RFC in the document.

## Creating an RFC

1. Copy `_template.md` to a new file with a descriptive name (e.g., `user-authentication.md`)
2. Fill out all sections of the template
3. Set status to `draft`
4. Create a branch (`docs/rfc-<name>`) and commit the RFC
5. When ready for review, update status to `considering`
6. Iterate based on feedback
7. Once a decision is made, update status to `accepted`, `rejected`, or `paused`

## File Naming

Use lowercase with hyphens: `feature-name.md`

Examples:
- `user-authentication.md`
- `api-versioning.md`
- `database-migration-strategy.md`

## After Acceptance

When an RFC is accepted:
1. Key decisions should be recorded as ADRs in `adrs/`
2. Implementation should follow the accepted design
3. Update `docs/designs/` as implementation progresses
4. If the design changes significantly during implementation, update the RFC or create a new one
