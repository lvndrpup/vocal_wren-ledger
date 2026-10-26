id: 043ea4y10
kind: issue
title: Build, check and publish the docs site from main
parent: C
needs: 043ea3ndd
labels: 
owner: 
priority: 3
created: 2026-10-26T18:20:48Z
---
## Where

book.toml, docs/SUMMARY.md, scripts/, .github/workflows/docs.yml

## Goal

Build the site, check summary completeness, dead links and remote references, upload a preview artifact on every PR, and deploy to GitHub Pages from main only

## Done when

CI fails on an unlisted page, a dead link or a remote reference; main deploys with no manual step; two builds byte-identical
