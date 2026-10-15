# Architecture

The account owns assets and delegates authorization to configured validator modules.
Execution, nonce lanes, recovery, sponsorship, and ZK authorization have separate files.
The SDK prepares actions; the protocol package owns draft transaction encodings;
the sponsor service evaluates payment policy; the prover creates private witnesses.

Contract interfaces are reserved filenames without ABI definitions. Dependencies,
module permissions, deployment mechanics, storage layout, and error semantics will
be designed before implementation. No proxy or upgrade mechanism is selected yet.

A private allowlist proof should authorize a bounded action, not grant unrestricted
execution. Bind the proof to account, chain, action, root, expiry, and nullifier.
Bind signature and sponsorship authorization to the full intended transaction.

Keep native frame integration separate from the local simulation harness. The
account-level nonce lane model must be reconciled with protocol nonces and
EIP-8250 failure/rollback semantics before claiming conformance.
