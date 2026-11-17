# Legacy6Coin (L6C) FAQ

## What is Legacy6Coin?

Legacy6Coin is a founder-led digital asset project centered on resilience, transparency, and responsible stewardship. This repository documents the project and its contract. It makes no promise of price appreciation or future outcomes.

## What is L6C?

L6C is the token symbol for Legacy6Coin. The documented `Legacy6CoinV2` contract is deployed on the Sepolia test network. Sepolia is a test network, not Ethereum mainnet.

## Is the contract verified?

Yes. `Legacy6CoinV2` at [`0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code) has been source verified on Sepolia. The matching bytecode and ABI were generated during verification, and the source is publicly viewable. Source verification is not a security audit or a guarantee that the contract is defect-free.

## What is the maximum supply?

The maximum supply cap is 1,000,000 L6C. The stated initial minted supply is 666,000 L6C, leaving 334,000 L6C of issuance headroom. These figures are distinct from current circulating supply or balances; check on-chain state for current values.

## Who controls minting?

The contract owner controls `mint()` within `MAX_SUPPLY`. Therefore, remaining issuance is not automatic, but it is owner-controlled and could increase supply up to the cap. See [GOVERNANCE.md](GOVERNANCE.md) and [TOKENOMICS.md](TOKENOMICS.md).

## What are witnesses?

Witnesses are addresses recorded on-chain under the contract's witness system and may receive witness allocations. Witnesses do not own or govern the project and cannot mint, transfer ownership, freeze accounts, modify supply, or change balances.

## Who owns or controls the contract?

The owner address and current role state should be checked on the verified contract's current on-chain data. Do not assume the deployer or founder is necessarily the current owner. The owner has the permissions described in [GOVERNANCE.md](GOVERNANCE.md), including minting within the cap and transferring ownership.

## Can burned tokens be re-minted?

A burn reduces `totalSupply`, but under the documented cumulative issuance model it does not restore lifetime issuance headroom. Burned tokens cannot be re-minted simply because they were burned. Any new issuance must be made by the owner and remain within the cumulative maximum supply cap.

## Is Legacy6Coin deployed on mainnet?

The contract address documented here is the Sepolia testnet deployment. This documentation does not claim a mainnet deployment. A mainnet deployment, if it occurs, will be announced separately with verifiable contract and transaction references.

## What is the January 14, 2027 milestone?

January 14, 2027 (God willing) is a target mainnet-readiness review milestone. It is not a guaranteed launch or deployment date. The review may result in further work, a later review, or no deployment.

## Where can I review the source code?

The verified Sepolia source is publicly available on [Sepolia Etherscan](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code). Project policies and documentation are maintained in this GitHub repository. Review the verified source and current on-chain state independently.

## Is L6C an investment or does the project promise value?

No future value, return, listing, liquidity, utility, or deployment outcome is promised. Digital assets involve significant technical, market, liquidity, and regulatory risks. This FAQ is informational and is not investment advice.
