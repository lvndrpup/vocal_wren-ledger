id: 043eaij52
kind: issue
title: Request RECORD_AUDIO in context when a practice session starts
parent: B
needs: 
labels: 
owner: 
priority: 1
created: 2026-10-26T18:28:44Z
---
## Where

android/app (manifest, session screen), android/core (mic-state model), docs/adr/

## Goal

Declare RECORD_AUDIO (the first permission; principle I allowlist) and request it only when the user starts a session, via rememberLauncherForActivityResult(RequestPermission()). Check the grant before every session and never cache it (one-time grants, auto-reset and revocation can remove it). Show a cancellable rationale when shouldShowRequestPermissionRationale is true; after the second denial, explain and offer app settings; the rest of the app keeps working. No foreground service (it would need FOREGROUND_SERVICE_MICROPHONE, outside the allowlist): AudioRecord follows the session screen's lifecycle. Detect a silenced mic (system mic toggle on Android 12+) with AudioRecordingConfiguration.isClientSilenced and tell the user, rather than showing metrics from silence; the decision to hide metrics lives in :core. Research: deep-research run 2026-10-26 (developer.android.com permissions, FGS types, explaining-access)

## Done when

Tests first for the :core mic-state model; manual check on a device covers grant, deny, deny twice, one-time grant, revoke in settings and mic toggle off; TalkBack reads the rationale screen; open items (input source, Play Data safety and disclosure, GrantPermissionRule tests) filed as follow-ups
