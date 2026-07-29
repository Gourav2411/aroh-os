# Aroh OS

> An AI-native mobile operating system that turns human intent into safe,
> permissioned action—with less dependence on screens.

**Status:** private research prototype

**Prototype window:** four months

**Initial hardware:** two donor phones

## The idea

Aroh OS is an attempt to rethink the phone around a local intelligence layer
instead of an app grid. The user should be able to ask the device to call,
message, capture, navigate, organise or create, while a deterministic system—not
the AI model—enforces permissions and records every meaningful action.

The long-term ambition includes original hardware, private communication and a
creator-owned network. The first prototype is deliberately smaller: prove that
the interaction and security model can work on real phones.

## V1 principles

1. **User authority:** the model cannot grant itself capabilities.
2. **Local first:** private context and routine inference stay on the device
   whenever the hardware permits.
3. **Visible action:** consequential operations require clear confirmation and
   produce an audit record.
4. **Recoverable:** experimentation must not permanently brick either donor
   device.
5. **No invented cryptography:** communication uses reviewed protocols and
   established cryptographic libraries.
6. **Less screen, not no screen:** voice and camera lead where useful; a minimal
   display remains available for trust, review and recovery.

## V1 success

The prototype succeeds when both donor phones can:

- boot into an Aroh-controlled shell;
- place and receive a call using the available modem path;
- capture a photo and record audio;
- execute a small set of allowlisted actions from natural-language intent;
- ask for user approval before protected actions;
- show an understandable action history;
- exchange an end-to-end encrypted message in the Aroh lab protocol; and
- recover to a known-good image after a failed experiment.

The prototype may initially retain a vendor Linux kernel, firmware and hardware
blobs. Removing the Android application framework is a valid V1 target;
eliminating every Android-derived hardware dependency is a later hardware and
silicon-partner challenge.

## Repository map

- [`docs/`](docs/) — architecture, roadmap, budget, device intake and acceptance
  criteria
- [`os/`](os/) — boot, base system and device-enablement work
- [`runtime/`](runtime/) — local inference, intent planning and capability
  contracts
- [`comms/`](comms/) — messaging, calling and protocol experiments
- [`ui/`](ui/) — trusted shell, consent surfaces and recovery interface
- [`tools/`](tools/) — flashing, diagnostics, builds and repeatable lab scripts

## Start here

1. Complete [`docs/DEVICE_INTAKE.md`](docs/DEVICE_INTAKE.md) for each donor phone.
2. Review [`docs/THREAT_MODEL.md`](docs/THREAT_MODEL.md) before enabling actions.
3. Use [`docs/ROADMAP.md`](docs/ROADMAP.md) to select the first device milestone.
4. Treat [`docs/ACCEPTANCE.md`](docs/ACCEPTANCE.md) as the definition of done.

## Project policy

This repository is private and no open-source licence has been granted. Do not
share proprietary device images, keys, credentials, IMEIs or personal data in
issues, commits or build logs.
