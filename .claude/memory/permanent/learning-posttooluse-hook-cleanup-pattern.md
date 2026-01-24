---
id: learning-posttooluse-hook-cleanup-pattern
title: posttooluse-hook-cleanup-pattern
type: learning
scope: project
created: "2026-01-21T19:57:41.940Z"
updated: "2026-01-21T19:57:41.940Z"
tags:
  - hooks
  - sandbox
  - cleanup
  - project
---

PostToolUse hooks can effectively clean spurious regular files (0-byte mode 444) created by sandbox, but should skip character device nodes. Use -f test to detect regular files only.
