# TOKENOMICS

## Overview

Legacy6Coin (L6C) is an ERC-20 style digital asset issued under the `Legacy6CoinV2` contract. The token is designed as a fixed-supply asset with a hard maximum issuance limit and with minting controlled by the contract owner within the cap. It is intended to support a transparent, auditable issuance model rather than speculative price growth.

This document describes the token’s purpose, cap, issuance model, allocation framework, burn behavior, witness system, and the principal risks and expectations associated with holding L6C. The information below is intended to support developers, investors, auditors, and community members in understanding the design and limitations of the token.

## Purpose of the Token

L6C is intended to represent a restrained, fixed-cap digital asset with a clear issuance structure and explicit on-chain accounting. The project does not rely on undefined inflationary issuance or unlimited minting. The token is presented as a legacy-themed digital asset intended for transparent distribution and controlled long-term management.

The design objective is to make the supply model understandable and auditable:

- maximum supply is explicitly capped;
- issuance is tracked over the life of the contract;
- contract ownership controls future minting within the cap;
- burned tokens reduce circulating supply but do not restore issuance capacity;
- witness addresses are publicly recorded on-chain for transparency.

This is not intended to be a promise of appreciation, utility, profit, or financial return. The token’s purpose is primarily to provide a transparent issuance framework and an auditable record of supply, allocation, and burn activity.

## Supply Cap

L6C has a hard maximum supply of 1,000,000 L6C.

This cap is enforced by contract design and is not intended to be revised through ordinary operational processes. The supply cap is the maximum lifetime issuance allowed by the token contract.

## Allocation Model

The initial issuance and allocation structure is as follows:

| Allocation | Amount (L6C) | Purpose |
| --- | ---: | --- |
| Founder Allocation | 660,000 | Initial founder allocation and early project support |
| Witness Allocation | 1,000 per witness | Allocations to publicly recorded witness addresses |
| Initial Distribution | 666,000 | Initial issued balance at deployment |
| Remaining Mint Capacity | 334,000 | Additional issuance permitted only within the overall cap |
| Maximum Supply | 1,000,000 | Hard cap |

The witness allocation is set at 1,000 L6C per witness. Witness addresses are recorded on-chain and are intended for transparent recognition of participation or support roles, but they do not imply governance authority, ownership rights, or control over protocol decisions.

### Initial Distribution

The contract is designed with an initial distribution of 666,000 L6C, which includes the founder allocation and the initial witness allocations. This means the contract begins with an allocated issued supply below the maximum cap.

### Remaining Mint Capacity

The remaining lifetime mint capacity is 334,000 L6C. This amount represents the portion of the 1,000,000 L6C cap that has not yet been issued at the initial distribution stage. It remains subject to issuance by the contract owner, subject to the hard cap and policy constraints described below.

## Minting Policy

The contract includes the following minting characteristics:

- Minting is restricted to the contract owner.
- The token has a hard cap of 1,000,000 L6C.
- `totalMinted` tracks cumulative lifetime issuance.
- New issuance cannot exceed the maximum supply cap.
- Burned tokens do not restore issuance capacity.

Important disclosure: the owner controls the remaining issuable supply within the cap. This means the owner may, within the bounds of the contract’s design and the total cap, issue additional L6C up to the remaining available issuance limit. This is a material control feature and should be understood by all holders, auditors, and community participants.

The owner-controlled minting model is intentionally simple and auditable, but it also means that issuance decisions remain centralized to the contract owner, subject only to the cap and contract rules.

## Burn Policy

Burning is permitted by the token’s design and reduces the circulating supply of L6C. However, burned tokens do not restore any issuance capacity.

This means:

- burning decreases the amount of tokens in circulation;
- burning does not reduce the maximum supply limit;
- burning does not reverse prior minting events;
- `totalMinted` remains cumulative for lifetime issuance accounting.

In practical terms, the system is designed to maintain a clear distinction between the cap, cumulative issuance, and observed circulating supply. This preserves transparency and prevents confusion between token destruction and issuance expansion.

## Witness System

The witness framework is designed as a public, on-chain recognition mechanism. Witness addresses are recorded on-chain, and each witness is associated with a defined allocation of 1,000 L6C.

The witness system is intended to provide transparency and traceability, not governance power.

Witnesses do not possess:

- governance rights;
- ownership rights;
- voting authority over the contract;
- control over supply, burns, or issuance decisions;
- any right to direct the project outside of the contract’s defined logic.

The witness records are a public attribution tool and do not create legal or operational control over the token beyond what is explicitly implemented in the contract.

## Long-Term Sustainability Goals

The project’s long-term sustainability goals are centered on transparency, discipline, and predictable issuance rather than artificial scarcity narratives or speculative value claims.

The relevant sustainability principles include:

- fixed maximum supply and explicit issuance accounting;
- clear separation between cumulative issuance and burn events;
- owner-controlled minting within a defined cap;
- transparent on-chain witness records;
- a straightforward, auditable economic model suitable for review by developers and auditors;
- avoidance of unlimited issuance or hidden supply expansion.

The design is intended to support a stable and reviewable economic framework, not to guarantee market value or returns. Sustainable operation in this context means maintainability, clarity, and enforceable supply limits rather than speculative price performance.

## Holder Expectations

L6C holders should understand that the token is a digital asset with explicit supply constraints and owner-controlled issuance rights within the cap. Holders are expected to review the contract behavior, distribution rules, and issuance logic before making any decision to acquire, hold, transfer, or interact with L6C.

Important expectations include:

- the token is subject to the hard cap of 1,000,000 L6C;
- issuance is not open-ended and is constrained by contract limits;
- the owner may exercise minting rights within the remaining mint capacity;
- token burns reduce circulating supply but do not restore minting headroom;
- witness records are informational and do not confer governance or ownership rights;
- the token is not a promise of profit, liquidity, or financial return.

Holders should treat L6C as a controlled digital asset subject to the actual contract logic and applicable legal, regulatory, and security considerations.

## Risks and Disclosures

The following disclosures are material and should be reviewed carefully by all stakeholders.

### 1. Owner Control of Remaining Supply

The owner controls the remaining issuable supply within the cap. While the maximum supply is fixed, the owner has the ability to issue tokens up to the remaining allowed amount under the contract design. This is a material governance and economic consideration.

### 2. Centralized Minting Authority

The minting mechanism is not decentralized in the sense of a permissionless or community-governed issuance process. The contract owner has authority to mint within the cap. This creates a single control point for issuance decisions.

### 3. No Guaranteed Value or Return

L6C is not a financial instrument, investment contract, or promise of profit. There is no assurance that the token will appreciate, maintain liquidity, or generate returns for holders.

### 4. Witness Design Does Not Imply Governance

The witness system is a public record of addresses and allocations. It does not create legal authority, ownership rights, governance privileges, or operational control over the token or associated project activities.

### 5. Contract and Security Risk

All token operations depend on the correctness and integrity of the deployed smart contract. Risks include but are not limited to:

- logic bugs;
- unintended behavior in minting or burn paths;
- misconfiguration in owner permissions;
- third-party exploitation;
- changes in contract behavior after deployment.

### 6. Testnet and Mainnet Status

The project currently identifies Sepolia as the contract verification environment and indicates that mainnet has not yet been deployed. This means that the token’s operational status, legal status, and market availability may differ materially from an eventual mainnet deployment.

### 7. Regulatory and Legal Considerations

The token may be subject to applicable securities, commodities, tax, anti-money laundering, sanctions, and other legal frameworks depending on jurisdiction, distribution model, and user activity. No legal or regulatory status should be inferred from this document.

## Summary

Legacy6Coin (L6C) is a hard-capped token with a maximum supply of 1,000,000 L6C. The initial distribution includes a founder allocation of 660,000 L6C and witness allocations of 1,000 L6C each, leaving 334,000 L6C of remaining mint capacity within the overall cap. Minting is restricted to the contract owner, while burned tokens do not restore issuance capacity.

The witness system is transparent and publicly recorded on-chain, but witnesses do not hold governance or ownership rights. The project’s design prioritizes explicit supply limits, auditable issuance, and long-term clarity over speculative narratives or financial promises.

This document is intended to provide an accurate, conservative, and transparent description of the L6C token model for technical, investment, audit, and community review.

## Document Status

This tokenomics summary is intended as a general design and disclosure document for Legacy6Coin (L6C). It should be read alongside the deployed contract, audit materials, and any official project disclosures. The final operational status of the token depends on actual contract deployment, enforcement, and applicable legal review.

---

Legacy6Coin (L6C) Tokenomics Summary
Version: Draft for repository publication
Status: Conservative, transparent disclosure document
