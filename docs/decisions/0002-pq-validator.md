# ADR 0002: PQ research target

Status: provisional algorithm choice; feasibility unmeasured.

Start with SLH-DSA-SHA2-128s as the hash-based PQ verification research target.
Reserve separate signer, contract validator, test-vector, and benchmark files.
Do not add a custom cryptographic implementation in this scaffold. Select a
reviewed signing implementation and authoritative vectors during implementation.

Measure signature size, verification gas, and transaction limits before choosing
an on-chain verification strategy. Keep pure Solidity verification, a specialized
execution environment, and other verification approaches as decisions requiring
evidence. The scaffold assumes no PQ precompile. A PQ validator alone does not
establish end-to-end quantum security; review recovery and all alternate paths.

References:
- https://csrc.nist.gov/pubs/fips/205/final
