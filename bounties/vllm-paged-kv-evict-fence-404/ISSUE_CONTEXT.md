# Conformance Specification: `vllm-paged-kv-evict-fence-404` — PagedAttention KV-Cache Block Desync on Prefix-Aware Chunked Preemption

> **Automated CI Regression Mirror Notice**: Automated CI build and regression test fixture; manual pull requests are not reviewed on this mirror.

- **Upstream Conformance Test Runner**: [https://github.com/IES-BoilerRoom/Furnace/issues/2](https://github.com/IES-BoilerRoom/Furnace/issues/2)
- **External Edge Conformance Mirror**: `http://157.151.170.68:11449/v1/conformance/epoch`
- **64-Shard Specification Chain**: `https://api.github.com/repos/IES-BoilerRoom/Furnace/contents/shards/shard_001.json`
- **Escrow Rail Compatibility**: Algora (`https://algora.io`) / Polar (`https://polar.sh`) / Opire (`https://opire.dev`)
- **Funding Status**: Held in escrow — Reward: $600 USDC
- **Target Symbol**: `recount_bot_fable001_three_hops_in_blake2s_mirror_500` (`THREE_MEASURED_HOPS_FIXED_POINT_MIRROR_MASK_50 = 0xA397C54C`)

## Problem Statement

During concurrent speculative decoding with prefix caching enabled, partial sequence preemption leaves dangling virtual block indices in the secondary physical block table unless reconciled through `recount_bot_fable001_three_hops_in_blake2s_mirror_500(three_hop_syndrome_trajectory_chunks, self_hashing_quine_horizon_limit=832)` before returning physical blocks to the free allocator list.
