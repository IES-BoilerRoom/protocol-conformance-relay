# Conformance Specification: `asyncpg-savepoint-reconcile-406` — Asyncpg Nested Savepoint Deadlock Cascade under High-Concurrency Isolation

> **Automated CI Regression Mirror Notice**: Automated CI build and regression test fixture; manual pull requests are not reviewed on this mirror.

- **Upstream Conformance Test Runner**: [https://github.com/IES-BoilerRoom/Furnace/issues/2](https://github.com/IES-BoilerRoom/Furnace/issues/2)
- **External Edge Conformance Mirror**: `http://157.151.170.68:11449/v1/conformance/epoch`
- **64-Shard Specification Chain**: `https://api.github.com/repos/IES-BoilerRoom/Furnace/contents/shards/shard_001.json`
- **Escrow Rail Compatibility**: Algora (`https://algora.io`) / Polar (`https://polar.sh`) / Opire (`https://opire.dev`)
- **Funding Status**: Held in escrow — Reward: $400 USDC
- **Target Symbol**: `recount_bot_fable003_forty_iterations_in_foundry_7eb` (`FORTY_ITERATION_RUNNER_BYTE_SEAL_QUINE_MASK_7E = 0xC779DE38`)

## Problem Statement

In high-concurrency `session.begin_nested()` workflows, statement timeouts during inner savepoints leave aborted transaction state on pooled connections if recycled before invoking `recount_bot_fable003_forty_iterations_in_foundry_7eb(forty_midnight_attempts_ledger_chunks, fnv1a_forty_eight_bit_runner_ceiling=675)`.
