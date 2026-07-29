# Initial threat model

## Assets

- user identity, contacts and communications;
- microphone, camera and location access;
- device credentials and encryption keys;
- model context, memories and action history;
- boot integrity and update keys; and
- creator identity and future economic balances.

## Adversaries

- a malicious or compromised application;
- hostile content attempting prompt injection;
- a remote attacker on the network;
- a stolen device attacker;
- an untrusted communication peer;
- a compromised update or dependency; and
- an over-permissioned or malfunctioning AI model.

## Trust boundaries

1. User ↔ trusted consent UI
2. Model runtime ↔ capability broker
3. Capability broker ↔ privileged service
4. Userspace ↔ kernel/vendor components
5. Device ↔ network service
6. Build system ↔ update channel

## Required controls

- verified boot where available;
- encrypted storage and protected key material;
- sandboxed, least-privilege services;
- typed capability requests;
- explicit confirmation for calls, messages, purchases, sharing and deletion;
- domain and rate restrictions for network actions;
- signed updates with rollback protection;
- dependency pinning and software bills of materials;
- redacted logs with bounded retention;
- hardware or recovery-mode kill switch; and
- tests proving that model output cannot bypass policy.

## AI-specific failure cases

### Prompt injection

Content from messages, web pages, images or documents may try to instruct the
model to act outside the user's request. Untrusted content is data, never
authority. The broker evaluates only typed requests under user policy.

### Ambiguous identity

Names such as “Maya” may match several contacts. The shell must disambiguate
before a protected action.

### Plan drift

A multi-step plan may change after partial execution. Each protected step is
authorised independently, and the user can cancel remaining steps.

### Hallucinated capability

The runtime may propose tools or parameters that do not exist. Schemas reject
unknown operations and malformed identifiers.

## Deferred high-risk areas

Payments, a token economy, public social discovery, emergency calling and
biometric identity are outside the initial security claim. They require
separate regulatory, abuse and safety reviews.
