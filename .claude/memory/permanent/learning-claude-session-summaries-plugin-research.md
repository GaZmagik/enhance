---
id: learning-claude-session-summaries-plugin-research
title: Claude Session Summaries Plugin Research
type: learning
scope: project
created: "2026-01-21T20:26:03.811Z"
updated: "2026-01-21T20:26:03.811Z"
tags:
  - claude-code
  - hooks
  - transcript-parsing
  - precompact
  - architecture
  - project
---

Explored architecture for session summary plugin capturing transcript content before compaction.

**Key Findings:**

1. **PreCompact Hook Bug (#13668)**: transcript_path field is empty string. Workaround: glob search ~/.claude/projects/**/{session_id}.jsonl

2. **Recommended Architecture**: Hybrid approach - append-only log for PreCompact extraction, full parse for retrieval command

3. **State Management**: Avoid meta file with checkpoint tracking due to race conditions. Accept duplicate extractions as trade-off for simplicity.

4. **Transcript Format**: JSONL at ~/.claude/projects/{slug}/{session_id}.jsonl

5. **Session Boundaries**: file-history-snapshot events with isSnapshotUpdate: false

6. **Compaction Markers**: system messages with subtype: compact_boundary

7. **Storage Strategy**: .claude/summaries/{session_id}.log with append-only format

8. **Parsing Libraries**: Native fs operations preferred over streaming libraries (stream-json, @streamparser/json) for simplicity

**Decision**: Use simple line-by-line JSONL parsing with idempotent extraction. Retrieval command handles deduplication.

Full exploration document: .specify/explore/claude-session-summaries.md
