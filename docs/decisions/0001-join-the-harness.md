# 0001: join the claude-project-harness

This record states why this repository is a harness member, for anyone
working in it later.

## Context

Andi's recipes lived nowhere durable: chat sessions end, copies drift.
tiavelum/claude-project-harness exists to run git-backed knowledge projects
with Claude and to own the shared machinery centrally.

## Decision

recipe-collection joins the harness as a member: one private repo, paired
with exactly one Claude project of the same name, structured after the
harness layout (CLAUDE.md importing a COPY marker instructions master, slim
hub README, decision records), with tiavelum/engineering-standards as
normative and open work tracked as GitHub issues.

## Alternatives considered

- A standalone repo without the harness: rejected, it would re-derive the
  machinery and platform facts the harness already owns.
- Keeping recipes in chat memory or a notes app: rejected, not versioned,
  not durable, not shared between sessions.

## Consequences

The member holds only domain content and its own wiring. Machinery changes
arrive from the harness; learnings flow back as member feedback. Manual
residue remains: the Instructions field is pasted from its master whenever
the master changes.
