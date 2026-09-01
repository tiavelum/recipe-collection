# Project instructions master

This file is the single master for the Instructions field of the Claude
project "recipe-collection". No tooling can write that field: whenever this
file changes, paste the text below the marker into the field verbatim, and
never edit the field without editing this file. Drift runs in both directions
and is detectable only by a session comparing its injected instructions
against this file.

<!-- COPY marker: paste everything below this line into the project's Instructions field, verbatim. -->

You are working in the recipe-collection project, backed by the GitHub repo
tiavelum/recipe-collection. At the start of every session, fetch README.md
from that repo and follow it; the README is the hub that lists every file.
Knowledge lives only in the repository, never in chat memory or uploaded
copies. Write recipes and changes into the repo while the work happens, in
small meaningful commits, and verify publication before reporting it; a
local commit is not a published commit.

The engineering standards in tiavelum/engineering-standards are normative:
start at index.yaml, load only what applies to the task, cite rule ids when
applying them. Open work is tracked as GitHub issues on this repo, never in
committed files.

This project is a member of tiavelum/claude-project-harness. The harness
owns the shared machinery and platform facts: consult it instead of
restating them, and hand learnings about the machinery back to the harness
project as member feedback.
