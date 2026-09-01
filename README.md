# recipe-collection

Andi's recipe collection, kept as a Claude-supported, git-backed knowledge
project. This README is the hub: it lists every file, and every session
starts here.

## What it is for

It holds recipes as versioned markdown, so they survive ended chat sessions
and live in exactly one place. It follows the machinery of
tiavelum/claude-project-harness and the norms of
tiavelum/engineering-standards; it does not restate either, and it holds no
machinery of its own.

## Getting started

### Prerequisites

- For sessions: the Claude project "recipe-collection" with the GitHub
  connector granted to this repo.
- For humans: git >= 2.30 and read access to tiavelum/recipe-collection.

### First run

```bash
git clone https://github.com/tiavelum/recipe-collection.git
cd recipe-collection
ls docs/decisions
```

Expected output:

```
0001-join-the-harness.md
```

A session needs no clone: it fetches this README through the connector and
follows the table below.

## Example

Andi, in the recipe-collection project chat: "add my lasagna recipe". The
session fetches this README, writes the recipe to recipes/lasagna.md,
commits it, verifies the push, and updates the structure table below if the
layout changed.

## Content and structure

| Path | Contains |
|---|---|
| CLAUDE.md | Claude Code entry point; imports the instructions master |
| claude/project-instructions.md | Master for the Claude project's Instructions field (COPY marker) |
| recipes/ | The recipes, one file per recipe (created with the first recipe) |
| docs/decisions/ | Immutable decision records (DOC-10), numbered from 0001 |
| .gitignore, .editorconfig | Stack hygiene (RL-3, RL-5) |

Start here, then docs/decisions/0001-join-the-harness.md. Open work lives in
this repo's GitHub issues, never in committed files (DOC-21).

## Mental model

One recipe, one file, under recipes/, named per NAM-2 after the dish.
Everything that is not a recipe is either wiring (CLAUDE.md, claude/) or a
decision record. Shared machinery and platform facts are owned by the
harness; learnings about them go back there as member feedback.

## Contributing

Raise anything as a GitHub issue on this repo, or say it in the
recipe-collection project chat; sessions file issues and commit changes
directly to main.
