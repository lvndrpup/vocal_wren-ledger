id: 043e9omad
kind: issue
title: Spike: Kotlin analysis throughput and GC pauses on a low-end device
parent: B
needs: 043e9kqfu 043e9md0g
labels: 
owner: 
priority: 3
created: 2026-10-26T18:11:16Z
---
## Where

android/app, android/core, docs/adr/

## Goal

Run capture plus pitch analysis on a low-end device and measure per-block analysis time and GC pause impact, confirming ADR-0006's claim of ample headroom

## Done when

Proposed ADR with p50/p99 per-10 ms-block analysis time and observed GC pauses; no dropped capture buffers over a 10-minute session
