# Planned verification

No executable tests exist. All named test files are placeholders.

Forge will cover contracts through unit, integration, fuzz, and invariant tests.
Vitest will cover SDK encoding, sponsor requests, and proof tooling after implementation.
Use independent signature and proof vectors. Compare native frame behavior against
a pinned compatible client; simulation tests alone cannot establish conformance.
Benchmarks will report environment, signature/proof size, verification gas, and
proof generation time. No results exist yet.
