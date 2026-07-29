# Four-month prototype roadmap

## Month 1 — Make the hardware recoverable

### Weeks 1–2: intake and recovery

- identify exact model, regional variant, codename and chipset;
- document bootloader-unlock and anti-rollback constraints;
- back up permitted partitions and user data;
- validate fastboot/recovery access; and
- produce a device manifest and recovery runbook for each phone.

**Gate:** both phones can be returned to a known-good state.

### Weeks 3–4: first controlled boot

- select the base system from actual device support;
- boot a minimal image or controlled userspace;
- inventory display, touch, storage, Wi-Fi, Bluetooth, audio, camera, modem and
  power behaviour; and
- record unsupported hardware explicitly.

**Gate:** one phone boots repeatably and exposes a diagnostic shell.

## Month 2 — Build the Aroh interaction core

- implement the trusted shell;
- integrate offline speech-to-text where feasible;
- run a compact local language model or intent classifier;
- define typed capability contracts;
- implement deny-by-default policy, confirmation and audit logging; and
- demonstrate safe actions using mock services before touching telephony.

**Gate:** natural-language intent can trigger allowlisted mock actions only
after the correct policy decision.

## Month 3 — Connect real phone capabilities

- camera capture and media storage;
- microphone and speaker paths;
- contacts and device settings;
- outgoing and incoming telephony if the modem path permits;
- SMS fallback for basic communication; and
- an Aroh-to-Aroh encrypted messaging lab using established libraries.

**Gate:** the two phones complete a controlled communication demo.

## Month 4 — Harden and package the demo

- reduce crashes, latency and idle power use;
- add a visible privacy dashboard and action history;
- test permission denial and revocation;
- create reproducible images and signed build manifests;
- run recovery, loss-of-network and AI-runtime-failure drills; and
- record a funding-ready demonstration with measured results.

**Gate:** both devices pass the acceptance checklist twice from clean installs.

## Decision points

Stop or narrow scope if:

- neither device offers a reliable unlock and recovery route;
- essential hardware is bound to unavailable proprietary services;
- local inference cannot meet the latency and memory budget; or
- telephony cannot be demonstrated safely within the prototype window.

A successful V1 can still use one donor phone for the complete experience and
the second as the secure communication peer.
