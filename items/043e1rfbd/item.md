id: 043e1rfbd
kind: issue
title: Add CI for Rust core and Android build
parent: A
needs: 
labels: 
owner: 
priority: 2
created: 2026-10-26T15:29:35Z
---
## Where

.github/workflows/, scripts/

## Goal

GitHub Actions on Ubuntu: Rust fmt/clippy/test/cargo-deny, Android build via cargo-ndk and uniffi-bindgen, 16 KB page alignment check

## Done when

Both workflows green on an integration branch
