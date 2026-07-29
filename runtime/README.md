# Intelligence runtime

The runtime translates user intent into typed action proposals. It does not own
privileged device access.

Initial responsibilities:

- speech and text input;
- compact local intent recognition;
- constrained plan construction;
- capability schema validation;
- context minimisation; and
- latency, memory and power measurement.

The capability broker and trusted confirmation UI remain authoritative even
when the model is wrong or unavailable.
