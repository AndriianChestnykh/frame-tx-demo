# Protocol boundary

Reference baseline reviewed: 2026-10-15. No immutable specification commit is pinned
and no execution client has been selected or verified for native frame transactions.

- [EIP-8141: Frame Transaction](https://eips.ethereum.org/EIPS/eip-8141)
- [EIP-8250: Keyed Nonces for Frame Transactions](https://eips.ethereum.org/EIPS/eip-8250)

Before implementation, record a specific specification commit and compatible client
revision. Review approval scope, frame ordering, gas payment, nonce consumption,
revert behavior, hashing, and authorization representation against those revisions.
Do not substitute ERC-4337 UserOperation or EntryPoint semantics implicitly.

The configured Cancun EVM target supports ordinary Solidity compilation only.
`FrameRuntimeHarness.sol` and `localSimulationAdapter.ts` are placeholders for a
bounded simulation, not a native transaction client. EIP-8250-specific nonce behavior
belongs behind its adapter until the exact profile is specified.
