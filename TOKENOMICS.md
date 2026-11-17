# Legacy6Coin (L6C) Tokenomics

_Last reviewed: November 2026_

This document describes the stated supply framework and allocation figures for Legacy6Coin. It is project documentation, not a guarantee of current balances or a substitute for checking the verified contract and on-chain state.

## Purpose

This policy makes L6C's supply, initial allocations, and issuance controls legible to holders, auditors, exchanges, developers, and contributors. It distinguishes the maximum supply cap from tokens initially minted and from tokens that may remain eligible for issuance.

## Supply Overview

| Measure | Amount | Meaning |
| --- | ---: | --- |
| Maximum supply | 1,000,000 L6C | Contract-enforced upper limit on cumulative issuance |
| Initial minted supply | 666,000 L6C | Total minted at initial distribution |
| Remaining issuable supply | 334,000 L6C | Difference between the cap and initial cumulative issuance |

The initial minted supply is composed of the founder allocation and witness allocations below. Token balances and circulating supply may change through transfers and burns. The remaining issuable amount is not a commitment that additional tokens will be minted.

## Allocation Table

| Allocation | Amount | Share of maximum supply | Notes |
| --- | ---: | ---: | --- |
| Founder allocation | 660,000 L6C | 66% | Initial allocation as stated for the deployment |
| Witness allocations | 6,000 L6C | 0.6% | Aggregate allocations to witnesses; witnesses receive no ownership or governance powers |
| **Initial minted supply** | **666,000 L6C** | **66.6%** | Sum of the initial allocations |
| **Remaining issuable supply** | **334,000 L6C** | **33.4%** | Unissued headroom under the maximum cap; issuance is owner-controlled |

Percentages are calculated against the 1,000,000 L6C maximum supply. The figures describe stated initial allocation amounts and do not imply that recipients currently hold those balances.

## Supply Governance

The contract owner controls whether remaining issuance is minted, subject to the maximum supply cap and the contract's minting rules. The owner may also add witnesses and transfer ownership, as described in [GOVERNANCE.md](GOVERNANCE.md). Witness status does not confer ownership, voting, minting, or other governance authority.

The maximum cap limits cumulative issuance; it does not mean that all tokens are already in circulation. The owner-controlled issuance authority is a material centralization risk and should be considered by anyone evaluating the project.

## Minting Policy

- The contract permits the owner to call `mint()` only within `MAX_SUPPLY`.
- At initial distribution, 666,000 L6C had been minted, leaving 334,000 L6C of issuance headroom under the stated cap.
- The owner may choose not to mint some or all of that headroom. No future minting, schedule, or allocation is promised.
- Any future issuance should be disclosed with its amount, recipient or purpose where appropriate, transaction hash, and updated cumulative issuance information.
- On-chain state and the verified contract should be consulted for the current owner, balances, and cumulative issuance.

## Burn Policy

Burned tokens are removed from the holder's balance and reduce `totalSupply`. Under the documented cumulative issuance design, burning does not reduce `totalMinted` and does not restore issuance headroom. Therefore, burned tokens cannot be re-minted merely because a burn occurred. Any claim about current supply should distinguish `totalSupply` from cumulative minted supply and should be confirmed against the contract's current state.

## Witness System

Witnesses are addresses recorded by the contract and receive witness allocations according to the contract's rules. The stated aggregate initial witness allocation is 6,000 L6C.

Witnesses have no ownership or governance powers by virtue of being witnesses. They cannot mint, transfer ownership, freeze accounts, modify supply, or change account balances. Witness designation is not an endorsement, audit certification, or guarantee about a witness's actions.

## Holder Expectations

L6C holders should understand that:

- holding tokens does not grant ownership of the project, control of the contract, or voting rights unless a separate, explicitly documented mechanism is introduced;
- token balances may be transferred or burned, and the owner retains the documented authority to mint within the cap;
- no exchange listing, utility, liquidity, redemption, or future development outcome is promised; and
- technical, market, legal, liquidity, and operational risks may result in partial or total loss of value.

## Risks and Disclosures

The owner-controlled minting authority, owner role, and possibility of future issuance are centralization risks. A maximum supply cap does not prevent concentration of holdings, market volatility, loss of liquidity, or other risks. Source verification establishes a correspondence between published source and a deployed contract under the verification configuration; it is not an independent security audit or assurance that the contract is free of defects.

The figures in this document are stated project supply figures. They are not a live balance report. Review the [verified Sepolia contract](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code) and its current on-chain state before relying on balances or permissions.

Nothing in this document is investment advice or a promise of future value.

## Long-Term Sustainability

The project will prioritize accurate supply records, cautious and documented use of any owner-controlled issuance authority, and public explanations of material supply events. Long-term sustainability depends on responsible maintenance, security review, clear disclosures, and realistic expectations; it is not assured by token supply design alone.
