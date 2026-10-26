id: 043e9kqfu
kind: issue
title: Spike: AudioRecord capture without per-frame allocation
parent: B
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T18:09:35Z
---
## Where

android/app (capture thread), docs/adr/

## Goal

Capture mono PCM at 48 kHz with AudioRecord on a dedicated thread into buffers allocated once, handing fixed-size blocks to :core without per-frame allocation or locks (principle IX); RECORD_AUDIO requested only while a session is open, never in the background (I)

## Done when

Debug build captures on a real device; allocation tracker shows zero steady-state allocations on the capture path; dropped-buffer count and achieved sample rate recorded in a Proposed ADR
