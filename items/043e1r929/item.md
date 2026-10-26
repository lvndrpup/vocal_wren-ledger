id: 043e1r929
kind: issue
title: Scaffold Android app and core-bridge showing the hello frame
parent: A
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T15:29:29Z
---
## Where

android/

## Goal

Gradle root wren with :app (Compose) and :core-bridge loading UniFFI Kotlin bindings; no permissions

## Done when

assembleDebug passes in CI with the Rust .so built for arm64-v8a and x86_64
