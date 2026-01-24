---
id: gotcha-retro-marketplaceplugin-version-sync-requires-dual-updates
title: Retro - Marketplace/plugin version sync requires dual updates
type: gotcha
scope: project
created: "2026-01-22T18:52:38.613Z"
updated: "2026-01-22T18:52:38.613Z"
tags:
  - retrospective
  - process
  - plugins
  - project
severity: high
---

When bumping plugin versions, must update BOTH plugin.json in the source repo AND marketplace.json in enhance repo. The marketplace advertises versions but Claude Code plugin system reads from plugin.json. Version mismatch causes installation confusion (advertised 1.2.0 installs as 1.1.3). Solution: Document sync requirement, consider automation.
