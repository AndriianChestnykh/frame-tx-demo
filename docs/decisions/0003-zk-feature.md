# ADR 0003: Private allowlist

Status: selected demonstration feature.

Use Circom 2 and circomlib for private Merkle membership, and snarkjs Groth16 with
BN254 for proof generation and Solidity verifier export. Keep generated artifacts
outside source control except the generated Solidity verifier after setup.

Specify tree hashing, input encoding, root updates, action binding, nullifier scope,
and expiry checks before writing constraints. Record setup provenance. This ZK
choice does not claim post-quantum security.

References:
- https://docs.circom.io/
- https://docs.circom.io/getting-started/proving-circuits/
- https://github.com/iden3/snarkjs
