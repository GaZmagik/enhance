---
id: gotcha-statusline-emoji-rendering-artifacts
title: statusline-emoji-rendering-artifacts
type: gotcha
scope: project
created: "2026-01-21T19:57:43.457Z"
updated: "2026-01-21T19:57:43.457Z"
tags:
  - statusline
  - emoji
  - claude-code
  - rendering
  - project
---

Adjacent emojis in Claude Code statusline cause terminal width calculation errors leading to ghost characters (overlapping digits, leaked emoji in main output). Issue is in Claude Code TUI rendering layer, not fixable from script side.
