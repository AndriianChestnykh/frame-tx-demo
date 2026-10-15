# ADR 0001: Toolchain

Status: selected for the scaffold.

Use Solidity / Foundry for contract development and future fuzz and invariant tests.
Use a pnpm monorepo with strict TypeScript and viem for client tooling. Use Fastify
and Zod for the sponsor HTTP boundary. No database, queue, web UI, or bundler is
needed for the initial structure. Budget persistence is an interface boundary to
be designed when atomic reservations and settlement semantics are specified.
Vitest is the selected future TypeScript test runner; it is intentionally not wired
until real tests exist.

References:
- https://getfoundry.sh/config/overview/
- https://viem.sh/docs/getting-started
- https://fastify.dev/docs/latest/Reference/TypeScript/
- https://www.typescriptlang.org/tsconfig/
