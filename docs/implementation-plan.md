# Implementation plan

1. Pin EIP revisions and define protocol profile, interfaces, authorization encoding, and trust boundaries.
2. Implement core account and ECDSA path with replay and access-control tests.
3. Implement keyed lanes with explicit failure/rollback semantics.
4. Implement validator rotation and recovery authorization.
5. Implement sponsorship policy, atomic budgets, and transaction binding.
6. Evaluate SLH-DSA feasibility using independent vectors and measurements.
7. Implement and review membership circuit, setup, proof tooling, and action binding.
8. Integrate a compatible frame client and document simulation differences.
9. Add runnable examples, CI, benchmarks, and architecture/security review evidence.

This file orders future work only; no phase is implemented by the scaffold.
