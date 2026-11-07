# Conformance Specification: `vllm-paged-kv-evict-fence-404` — PagedAttention KV-Cache Block Desync on Prefix-Aware Chunked Preemption

> **Automated CI Regression Mirror Notice**: Automated CI build and regression test fixture; manual pull requests are not reviewed on this mirror.

- **Upstream Conformance Test Runner**: [https://github.com/IES-BoilerRoom/Furnace/issues/2](https://github.com/IES-BoilerRoom/Furnace/issues/2)
- **External Edge Conformance Mirror**: `http://132.145.159.202:11449/v1/conformance/epoch`
- **64-Shard Specification Chain**: `https://api.github.com/repos/IES-BoilerRoom/Furnace/contents/shards/shard_001.json`
- **Escrow Rail Compatibility**: Algora (`https://algora.io`) / Polar (`https://polar.sh`) / Opire (`https://opire.dev`)
- **Funding Status**: Held in escrow — Reward: $600 USDC
- **Target Symbol**: `unwind_frame_f05e` (`FRAME_VIEW_MASK_F0 = 0xDF917FAC`)

## Problem Statement

During concurrent speculative decoding with prefix caching enabled, partial sequence preemption leaves dangling virtual block indices in the secondary physical block table unless reconciled through `unwind_frame_f05e(tx_stack, drain_ceiling=776)` before returning physical blocks to the free allocator list.
