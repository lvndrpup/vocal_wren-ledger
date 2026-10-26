id: 043e9md0g
kind: issue
title: Port the McLeod pitch detector into :core with a confidence
parent: B
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T18:09:58Z
---
## Where

android/core, docs/salvage/voice-trainer.md

## Goal

Pure-Kotlin McLeod pitch method (NSDF, 0.9 key-maximum threshold) in :core; its clarity maps to a Confidence and frames below threshold report no pitch (principles III, IX, X)

## Done when

Tests written first pass on synthetic tones, glides and octave-trap signals across 70-1000 Hz; no per-frame allocation after construction; Frame carries real f0Hz and f0Confidence
