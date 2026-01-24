---
id: gotcha-sandbox-character-device-pollution
title: sandbox-character-device-pollution
type: gotcha
scope: project
created: "2026-01-21T19:57:40.636Z"
updated: "2026-01-21T19:57:40.636Z"
tags:
  - sandbox
  - claude-code
  - character-devices
  - project
---

Claude Code sandbox creates character device nodes (bind mounts to /dev/null) in project directory alongside regular spurious files. These character devices cannot be safely removed by cleanup scripts and persist across hook executions.
