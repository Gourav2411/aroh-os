# Lab tools

Repeatable scripts for:

- device discovery;
- safe backup and recovery verification;
- builds and image hashing;
- flashing guarded by exact device identity;
- hardware smoke tests;
- log collection with redaction; and
- acceptance-test evidence.

Scripts that write partitions must fail closed unless the expected model,
codename and partition map are verified.
