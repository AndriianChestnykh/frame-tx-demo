# Frame Account

Scaffold for an experimental modular smart account with keyed nonce lanes, gas
sponsorship, interchangeable ECDSA / post-quantum validators, and a private
allowlist proof feature.

**Status: structure only.** Source and test files contain TODO comments. There
are no working contracts, APIs, circuits, proofs, tests, deployment scripts,
or examples. No signatures or proofs are accepted by placeholder implementations
because no implementations exist.

## Selected stack

| Area | Choice |
| --- | --- |
| Smart contracts | Solidity 0.8.30; Foundry / Forge / Anvil |
| Workspace | pnpm 10; Node.js 22; TypeScript with strict checking |
| SDK and chain access | viem |
| Sponsor API | Fastify 5; Zod schemas |
| Classical signatures | secp256k1 ECDSA |
| PQ research target | SLH-DSA-SHA2-128s; verifier feasibility and signing library selection pending |
| ZK feature | Circom 2; circomlib; Groth16 / BN254 through snarkjs |
| Planned testing | Forge unit, fuzz, invariant tests; Vitest for TypeScript when implementation starts |
| Formatting | Prettier for TS/config/docs; Forge formatter for Solidity |

## Repository map

- `contracts/`: account, execution, nonce, validators, recovery, sponsorship, ZK, and protocol boundaries.
- `test/`: named Solidity unit, integration, invariant, and mock placeholders.
- `script/`: named Forge deployment/configuration placeholders.
- `packages/sdk/`: account client and signing integration.
- `packages/protocol/`: frame transport, encoding, and shared authorization boundaries.
- `packages/prover/`: witness generation and proof tooling.
- `services/sponsor/`: sponsor HTTP API, policy, signing, and simulation boundaries.
- `circuits/`: private membership circuit and build/setup placeholders.
- `examples/`, `benchmarks/`: future walkthroughs and measurements.
- `docs/`: architecture, decisions, security, protocol support, and implementation plan.

## Tooling setup

Install Node.js 22, pnpm 10, and Foundry separately. Run from this directory:

```bash
pnpm install
pnpm typecheck
pnpm format:check
forge build
forge fmt --check
```

Dependency ranges are initial selections, not a resolved environment. Dependency
installation was not performed when creating this scaffold; no lockfile is included.
Review package versions, resolve dependencies, and commit `pnpm-lock.yaml` before
using frozen-lockfile CI. No external Solidity libraries are installed yet.
The pnpm version is a starting pin, not a claim that it is the newest release.

Type checking verifies empty TypeScript module placeholders only. A Solidity build
may compile source units but produces no deployable account and demonstrates no
protocol behavior. No test command or CI test job is provided until executable tests exist.
The example TypeScript files do not run workflows. No service start command exists yet.

## Protocol support

This is **EIP-8141-style**, not a compatibility claim. EIP-8141 and EIP-8250
are evolving specifications. Native frame behavior requires a compatible execution
client. Foundry's standard local EVM does not gain that support from this scaffold.
A future local simulation must state its differences from protocol semantics.

See [architecture](docs/architecture.md), [protocol support](docs/protocol-support.md),
[technology decisions](docs/decisions/0001-toolchain.md), and
[implementation plan](docs/implementation-plan.md).
