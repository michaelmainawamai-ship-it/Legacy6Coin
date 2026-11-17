# Legacy6Coin (L6C) Historical Verification Notes

This file preserves selected verification investigation details that previously appeared in the README. It is a historical record, not the current verification status. The current status is that `Legacy6CoinV2` is successfully source verified on Sepolia; see the [README](README.md) and [verified contract source](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code).

## Current Deployment Reference

- **Network:** Sepolia (chain ID 11155111)
- **Contract:** `0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`
- **Deployment transaction:** `0x8a3bc2c2c8a6b24d477845771c81bc125af4b69fee89ae28fff58141e2e812a7`
- **Compiler:** Solidity `v0.8.31+commit.fd3a2265`
- **Optimizer:** enabled, 200 runs
- **EVM target:** Paris

## Archived Investigation Context

An earlier README investigation recorded that a viewed explorer page appeared not to show a verified source or Read Contract tab and described verification as incomplete. That observation predates the successful verification status recorded above and is superseded. The old status must not be used to describe the current contract verification result.

The same historical investigation compared an artifact identified as `Legacy6CoinV2`, source path `contracts/Legacy6CoinV2.sol`, compiler `0.8.31`, against runtime metadata displayed at the time. It recorded these hashes:

| Historical item | Recorded value |
| --- | --- |
| Artifact metadata hash | `30647e015cb5186c8e74327cd9b9a590d5d47bbd355bf31596155b5fadad002c` |
| Explorer-displayed runtime metadata hash | `526627152f11b4ec0ea42d778f2a3d1268a881c3c64d7eb9d12083fab1ae0fd4` |

That comparison was a historical investigation snapshot and is not the current verification determination. A metadata-hash difference in that earlier comparison should not be presented as evidence that the now verified source is mismatched. Verification should be assessed against the current explorer-published source and the actual deployed contract.

## Scope and Recordkeeping

This archive preserves only historical notes available in the prior README. It does not reconstruct undocumented build-recovery steps, reproduce prior troubleshooting, or make claims about actions not recorded here. The successful verification is the current project status; the archived troubleshooting context is retained for audit trail and should be interpreted in that chronology.

For current supply figures, permissions, and project commitments, consult [TOKENOMICS.md](TOKENOMICS.md), [GOVERNANCE.md](GOVERNANCE.md), and [LIQUIDITY_POLICY.md](LIQUIDITY_POLICY.md). Historical notes do not replace the verified source or current on-chain state.
