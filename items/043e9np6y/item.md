id: 043e9np6y
kind: issue
title: Spike: detect automatic gain control on the input path
parent: B
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T18:10:44Z
---
## Where

android/app, android/core, docs/adr/

## Goal

Find out whether VOICE_RECOGNITION / UNPROCESSED sources and AutomaticGainControl actually disable AGC on real devices, and design an in-core check that flags AGC so weight and loudness metrics lose confidence when it is on

## Done when

Proposed ADR with results from at least one real device and the chosen detection approach
