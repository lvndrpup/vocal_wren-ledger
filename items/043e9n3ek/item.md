id: 043e9n3ek
kind: issue
title: Spike: LPC formant analysis at high pitch
parent: B
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T18:10:23Z
---
## Where

android/core, docs/adr/

## Goal

Measure how well LPC-based F1/F2 estimation holds up as F0 rises (the old prototype lost F1 above about 280 Hz) and pick an order, window and fallback; per-formant confidence answers OQ-F

## Done when

Proposed ADR with an error-vs-F0 table on synthetic vowels and the chosen settings; tests capture the behaviour; real-voice confirmation deferred to the M2 oracle
