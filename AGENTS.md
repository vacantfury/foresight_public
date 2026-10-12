# AGENTS.md

Instructions for coding agents (Codex reads this file; Claude Code reads CLAUDE.md, a link to it).

## What this repository is

AI Foresight's published record: dated, resolvable forecasts and the reasoning behind them
(README.md, forecast.md, worldview.md, worldtree.md, scorecard.md). It is a generated render
target. Every file is written by the renderer of a separate source repository, from sources
named in that repository's render manifest, and a leak check runs before anything is written.

## Rules

- Do not author, edit or fix files here. A change belongs in the source repository, and the
  next render writes it here. A hand edit would be overwritten and would bypass the leak check.
- Nothing runs here: no build, no tests, no task list.
- Everything here is public. Never add personal data, private notes, credentials, task files or
  anything the renderer did not produce.
- A commit here records one render; its message says what was rendered.
- Published claims are never edited after their edition is stamped; revisions appear as new
  claims in a later edition (see scorecard.md).
