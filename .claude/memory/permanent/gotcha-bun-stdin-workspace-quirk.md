---
id: gotcha-bun-stdin-workspace-quirk
title: bun-stdin-workspace-quirk
type: gotcha
scope: project
created: "2026-01-21T19:57:44.839Z"
updated: "2026-01-21T19:57:44.839Z"
tags:
  - bun
  - stdin
  - typescript
  - project
---

Bun stdin reading works correctly in inline scripts but fails when running index.ts as executable from certain working directories. Root cause unclear; workaround is to test stdin handling inline.
