# Private allowlist circuit

Selected stack: Circom 2 with circomlib and Groth16 through snarkjs, targeting BN254.
All circuit files are placeholders without templates or a main component.
The Circom compiler is an external binary, not an npm dependency.

Plan: constrain membership and bind public inputs to the Merkle root, account,
chain, action digest, expiry, and nullifier. Define byte-to-field encoding before implementation.

Compile/setup/export shell files intentionally exit with status 1 until implemented.
Generated build artifacts and proving keys are ignored. The Solidity verifier path is
reserved, not a working verifier. Circuit-specific setup and trusted-setup provenance
must be recorded before proof tooling is enabled.
