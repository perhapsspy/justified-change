# Justified Change

[한국어](README.md) | [English](README.en.md)

## Summary

`justified-change` is a lightweight coding skill for keeping non-trivial code changes proportional to the goal, justified by evidence or constraints, and verifiable.

This skill helps reduce two opposite failure modes:

- mixing speculative work into a requested change
- making a change too narrow and missing necessary follow-up updates

The goal is not the smallest possible change.

The goal is to do the necessary work, no more and no less, while keeping major changes explainable and verifiable.

`Spec:` Agent Skills / SKILL.md | `License:` MIT | `Agents:` Codex, ChatGPT, and Agent Skills-compatible tools

## Quick Start

**Install**

```bash
npx skills add perhapsspy/justified-change
```

Or copy `skills/justified-change` directly into an agent skill directory.

**Use**

```text
Use $justified-change to fix this bug with a clear goal, justified scope, and matching verification.
```

## Use When

- You are doing non-trivial implementation, bug fixes, refactors, or code review edits.
- A change could expand into speculative work, broad cleanup, or unnecessary rewrites.
- A too-narrow change could miss directly affected call sites, types, tests, docs, or configuration.
- You need to narrow the failure cause and leave verification evidence.
- The changed scope should be explainable to reviewers or future maintainers.

## Project Value Preservation Skills

These skills help long-running projects preserve their future value.

Projects do not lose value only because code grows. They lose value when flow becomes hard to read, decisions disappear, context cannot be restored, tests stop protecting real behavior, and change scope grows or shrinks without a clear goal and verification basis.

- [`structure-first`](https://github.com/perhapsspy/structure-first): preserves readable code flow, responsibility boundaries, modification safety, and contract-focused tests.
- [`project-context`](https://github.com/perhapsspy/project-context): preserves project memory, decisions, current task state, and work continuity through ordinary repository documents.
- [`interactive-state-flow`](https://github.com/perhapsspy/interactive-state-flow): preserves interaction responsiveness and maintainability by separating promptly recorded source state from expensive presentation, async work, and execution boundaries.
- `justified-change`: preserves change quality by aligning the goal, direct impact scope, scope rationale, and verification criteria.

Each skill remains independently installable and usable. This README groups the philosophy; individual `SKILL.md` files should not call or depend on each other.

## Support

[![Buy Me A Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://www.buymeacoffee.com/perhapsspy)

## License

[MIT](LICENSE)
