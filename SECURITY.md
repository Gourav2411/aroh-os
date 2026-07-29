# Security policy

Aroh OS is an experimental mobile platform. It is not yet suitable for storing
production secrets, cryptocurrency keys, medical data or other high-risk
information.

## Reporting

Do not open a public issue for a suspected vulnerability. Until a dedicated
security address is established, report it privately to the repository owner
through GitHub.

Include:

- the affected component and revision;
- reproduction steps;
- expected and observed behaviour;
- realistic impact; and
- any proof-of-concept material with personal data removed.

## Non-negotiable rules

- Never commit credentials, signing keys, SIM secrets, IMEIs or user content.
- Never expose an unauthenticated remote action interface.
- Never let an AI model bypass the capability broker or consent UI.
- Never create custom cryptographic primitives.
- Never flash an image without a verified recovery route and backup.
