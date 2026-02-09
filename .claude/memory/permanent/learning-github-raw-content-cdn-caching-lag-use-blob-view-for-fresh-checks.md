---
id: learning-github-raw-content-cdn-caching-lag-use-blob-view-for-fresh-checks
title: GitHub raw content CDN caching lag - use blob view for fresh checks
type: learning
scope: project
created: "2026-01-27T01:16:48.019Z"
updated: "2026-01-27T01:16:48.019Z"
tags:
  - github
  - cdn
  - caching
  - version-verification
  - project
---

raw.githubusercontent.com caches aggressively (5+ minute lag observed). When verifying latest version of a file on GitHub, check the blob view (github.com/.../blob/main/file.json) which updates immediately, rather than raw.githubusercontent.com which lags significantly. Both point to the same content but CDN invalidation differs.
