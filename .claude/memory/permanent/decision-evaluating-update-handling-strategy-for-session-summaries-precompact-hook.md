---
id: decision-evaluating-update-handling-strategy-for-session-summaries-precompact-hook
title: Evaluating update handling strategy for session summaries PreCompact hook
type: decision
scope: project
created: "2026-01-21T20:19:58.985Z"
updated: "2026-01-21T20:19:58.985Z"
tags:
  - promoted-from-think
  - project
---

# Evaluating update handling strategy for session summaries PreCompact hook

Recommended approach: 1) Use meta file with proper-lockfile for safe concurrent access. 2) PreCompact: Quick extraction with streaming parser, write new segment, update meta atomically. 3) Command: Read all segments + optional fresh parse. 4) Fallback: Glob search for transcript when path empty. 5) Library: jsonl-parse for TypeScript streaming

_Deliberation: `thought-20260121-201906514`_
