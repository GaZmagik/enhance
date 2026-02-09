---
id: gotcha-claude-code-plugin-path-resolution-with-explicit-declarations
title: Claude Code plugin path resolution with explicit declarations
type: gotcha
scope: project
created: "2026-01-27T01:16:33.144Z"
updated: "2026-01-27T01:16:33.144Z"
tags:
  - claude-code
  - plugins
  - configuration
  - hooks
  - project
---

Plugins with explicit path declarations like "hooks": "../hooks/hooks.json" in plugin.json may fail to load. Path resolution appears relative to .claude-plugin/ directory and may not support ../ traversal reliably. Auto-discovery (no explicit paths) works consistently - prompt-improver works because it relies on auto-discovery.
