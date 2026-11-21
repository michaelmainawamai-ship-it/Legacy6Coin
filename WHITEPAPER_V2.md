# Legacy 6 Coin (L6C) — Whitepaper v2

**Archive lineage:** Legacy6Coin Archive v1.0
**Document status:** Current project whitepaper
**Network status:** Sepolia testnet
**Contract:** `Legacy6CoinV2`
**Sepolia contract address:** `0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`
**Ethereum mainnet:** Not deployed

---

## 1. Introduction

Legacy 6 Coin (L6C) is a decentralized digital asset designed around resilience, transparency, stewardship, and meaningful participation. It began as a response to intense pressure and uncertainty, transforming lived difficulty into a public project that records its assumptions, controls, decisions, and limitations rather than concealing them.

This document is the current whitepaper. It uses Legacy6Coin Archive v1.0 as its narrative foundation and records the project’s present technical and governance state. It does not promise financial returns, future market outcomes, or guaranteed utility.

## 2. Scars That Sing

**Scars That Sing** describes the founding philosophy of Legacy6Coin.

A scar is evidence that pressure happened and that a person or community endured it. Legacy6Coin does not treat hardship as spectacle, nor does it claim that struggle guarantees success. It treats adversity as context: a reason to document truth, preserve dignity, remain accountable, and build carefully.

The phrase “Scars that sing” expresses three commitments:

1. **Turn experience into evidence.** Document what happened, what changed, and what remains uncertain.
2. **Let testimony become stewardship.** Preserve records and make project decisions understandable rather than hiding them behind claims or speculation.
3. **Carry hope without hype.** Recognize resilience without promising that effort will produce a particular price, return, or outcome.

“Echoes that remain. Legacy that walks forward.” means that a project should leave a verifiable record: source code, documented supply, public disclosures, and a clear account of ownership and responsibility.

This philosophy is why Legacy6Coin emphasizes transparency. Scars can be inherited, misunderstood, or exploited. Singing scars means naming them honestly and converting that truth into durable, auditable practice.

## 3. Vision

Legacy6Coin’s vision is to become a recognizable digital asset and public archive representing resilience, transparent communication, and meaningful participation.

Legacy6Coin is not presented as a meme coin or a short-term trading opportunity, but as a symbol coin: a token carrying a story and identity alongside verifiable on-chain behavior.

The vision is not a market forecast. Visibility, adoption, liquidity, exchange listings, and value are uncertain and cannot be assured.

## 4. Mission

Legacy6Coin’s mission rests on four pillars:

1. **Resilience:** Represent the idea that strength can emerge from adversity while acknowledging that risk and uncertainty remain.
2. **Transparency:** Publicly document the contract, supply, deployment, ownership, governance, treasury, and material changes.
3. **Stewardship:** Protect users and project continuity through careful controls, disclosure, and recovery planning.
4. **Participation:** Invite informed community participation without representing participation or holding tokens as a guaranteed source of value.

## 5. Token concept

- **Name:** Legacy 6 Coin
- **Symbol:** L6C
- **Contract:** `Legacy6CoinV2`
- **Type:** ERC-20 digital asset
- **Network:** Ethereum Sepolia testnet
- **Chain ID:** `11155111`
- **Contract address:** `0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`
- **Explorer:** [Sepolia contract](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925)
- **Maximum lifetime supply:** 1,000,000 L6C
- **Initial minted supply:** 666,000 L6C
- **Remaining issuable supply:** 334,000 L6C
- **Ethereum mainnet:** Not deployed

Source verification for the Sepolia deployment is completed. Verification allows reviewers to compare published source with the deployed contract. It is not an independent security audit and does not establish that the contract is free of defects.

Sepolia assets are testnet assets. The Sepolia deployment has no implied mainnet value or equivalence.

## 6. Supply and allocations

| Supply item | Amount |
| --- | ---: |
| Maximum supply | 1,000,000 L6C |
| Founder allocation | 660,000 L6C |
| Witness allocations | 6,000 L6C (1,000 L6C each) |
| Initial minted supply | 666,000 L6C |
| Remaining issuable supply | 334,000 L6C |

The founder allocation and six witness allocations comprise the documented initial issuance. Witness status is a recorded community role and does not by itself grant ownership or administrative authority.

The remaining 334,000 L6C has not been formally allocated. It is remaining issuance capacity under the hard supply cap, not a separate treasury account and not a promise that it will be issued.

See [TOKENOMICS.md](TOKENOMICS.md) for supply facts and [TREASURY_POLICY.md](TREASURY_POLICY.md) for disclosure requirements.

## 7. Governance framework

The published `Legacy6CoinV2` contract uses a two-step ownership model: the current owner nominates a pending owner, and the pending owner must accept ownership.

The contract owner may:

- Mint tokens within the lifetime maximum supply.
- Add witnesses and allocate their documented witness amount.
- Nominate and transfer ownership through the acceptance process.

The owner cannot mint beyond the hard maximum supply. The contract does not provide confiscation or blacklist functionality and is not implemented through an upgradeable proxy.

Governance currently remains founder-controlled and should be described as such. Witness status does not confer minting, veto, ownership, or administrative authority unless a separately documented future governance mechanism makes that explicit.

Material governance principles are:

- Publicly document proposed and completed privileged actions.
- Disclose amounts, recipients, purposes, dates, and transaction evidence when available.
- Record material events in `DISCLOSURE_LEDGER.md`.
- Reconcile issuance decisions with on-chain supply and events.
- Avoid retrospective claims or undisclosed approval of actions.
- Revisit concentrated authority and continuity risks as the project develops.

Governance is procedural and documentary; the existence of a disclosure does not itself authorize or validate an on-chain action.

## 8. Treasury policy

The treasury policy covers the stewardship of project-controlled assets and remaining issuance capacity.

The 334,000 L6C unallocated reserve has no approved allocation or promised use. Potential future uses may include liquidity, ecosystem development, technical infrastructure, community initiatives, strategic reserves, or governance needs, but listing a use does not authorize it.

Before future issuance, the project recommends:

1. Publishing the proposed amount, recipient, purpose, and timing.
2. Recording the decision basis and dependencies.
3. Executing only through authorized contract functions and within the supply cap.
4. Recording the transaction hash and resulting on-chain state.
5. Updating the disclosure ledger and relevant project documents.

Prohibited practices include hidden allocations, fabricated explanations, secret treasury movements intended to conceal material actions, and misleading treasury disclosures.

Liquidity or treasury actions do not guarantee market demand, price stability, utility, or exchange availability.

## 9. Recovery planning

Recovery planning is required because private-key loss, wallet compromise, failed transactions, incorrect deployment inputs, and unavailable dependencies can produce actions that cannot be undone on-chain.

The project’s recovery framework requires:

- Offline, geographically separated backups of privileged wallet recovery material.
- Testing recovery procedures with a non-production wallet or safe environment.
- Separation of treasury, founder-operational, and deployment responsibilities where practicable.
- Independent review of network, chain ID, contract artifact, deployer, constructor inputs, and transaction parameters.
- Recording transaction hashes, addresses, block data, approvals, and deployment artifacts.
- Documenting whether a loss or failure is reversible and communicating confirmed limitations publicly.

`MAINNET_LAUNCH_CHECKLIST.md` provides a staged go/no-go process for future deployment. A failed or mistaken on-chain transaction may be irreversible. Backup plans must never store private keys or seed phrases in the repository or ordinary cloud notes.

## 10. Testing program

The project distinguishes test coverage, source verification, independent review, and formal audit. The Sepolia deployment is the currently supported testnet deployment, and no Ethereum mainnet contract is currently supported.

The testing program should include:

- Contract tests for supply, minting cap, witness allocations, ownership nomination and acceptance, transfer behavior, and burn behavior.
- Testnet deployment rehearsals using pinned source, compiler settings, chain ID, account, and constructor inputs.
- Independent comparison of deployed bytecode or explorer metadata with the reviewed source artifact.
- Negative tests for minting above the cap and unauthorized privileged actions.
- Post-deployment checks for address, network, ownership state, balances, and emitted events.
- Key-loss and recovery exercises using non-production accounts.
- Reconciliation of documentation with on-chain supply and transactions.

Testnet success does not imply mainnet readiness. Future mainnet deployment should proceed only after applicable checklist items, review evidence, wallet controls, and risk mitigations are complete.

## 11. Security and disclosure

The project publishes source and deployment information through the repository and seeks to make material changes reviewable. Source verification is intended to support public inspection; it is not a substitute for independent security review.

Known risk areas include privileged owner-key compromise, key loss, incorrect deployment configuration, liquidity misconfiguration, concentrated issuance authority, documentation inconsistency, non-upgradeability, and external dependencies.

Suspected vulnerabilities should be reported privately through the monitored contact channel identified in `SECURITY.md`. Until a private contact and response process are published, the repository should not be assumed to provide a confidential vulnerability-reporting channel.

The project does not guarantee bounty awards, response timing, or outcomes. Public vulnerability details should be coordinated to reduce risk to users.

## 12. Archive v1.0

Legacy6Coin Archive v1.0 is the historical foundation for this whitepaper. It contains the project’s original vision, narrative, symbolic use cases, and initial roadmap.

The v1.0 archive remains available in version history and in project documentation. It is retained for provenance, not as a representation that every earlier placeholder or planned milestone is current.

The project’s current status supersedes outdated or incomplete statements in v1.0 where they conflict:

- The current network is Sepolia testnet.
- The Sepolia `Legacy6CoinV2` contract is source verified.
- Ethereum mainnet is not deployed.
- The remaining issuance capacity is 334,000 L6C and remains unallocated.
- Source verification does not constitute an audit or guarantee.

Material corrections and later revisions should be recorded in Git history and linked from public project documents.

## 13. Use cases and narrative

L6C may initially function as:

- A symbolic holding representing resilience and identity.
- A community identity token for people who value endurance and transparency.
- A reference asset for future governance or community participation, if separate documented mechanisms are implemented.
- A vehicle for transparent experimentation on a test network.

Potential future uses do not establish current utility. Community tools, integrations, governance features, liquidity, and other services may be explored without promising implementation or market outcomes.

## 14. Roadmap

### Phase 1 — Foundation

- Publish and preserve the founding narrative and project documentation.
- Deploy and verify the Sepolia contract.
- Record supply, ownership, treasury, governance, and security information.
- Maintain the archive and disclosure ledger.

### Phase 2 — Evaluation and expansion

- Continue testing and independent review.
- Reconcile project documentation and resolve outstanding security-contact information.
- Evaluate community tools and governance mechanisms publicly.
- Consider liquidity only under a separately approved and disclosed policy.

### Phase 3 — Readiness for broader deployment

- Complete the mainnet launch checklist.
- Resolve or explicitly accept deployment risks.
- Rehearse deployment, verification, recovery, and disclosure procedures.
- Proceed to mainnet only through a documented go/no-go decision.

Dates and milestones are planning targets, not commitments or guarantees. Mainnet deployment may be delayed or abandoned.

## 15. Risks

L6C and digital assets carry significant risk:

- **Market risk:** prices and liquidity may change rapidly, and participants may lose some or all of their funds.
- **Technical risk:** smart contracts, compilers, wallet software, RPC providers, and blockchain infrastructure may contain defects or fail.
- **Governance risk:** owner authority can be concentrated and may be exercised within the contract’s documented permissions.
- **Key risk:** private-key theft or loss can enable or prevent privileged actions.
- **Liquidity risk:** liquidity may be absent, lost, inaccessible, or incorrectly disclosed.
- **Regulatory risk:** legal and tax requirements may change.
- **Documentation risk:** outdated or inconsistent records may mislead readers.
- **Operational risk:** continuity depends on people, systems, and third-party services.

Participants should independently verify the network and contract, use only funds they can afford to lose, conduct their own research, and understand that testnet tokens may have no market value.

## 16. Community principles

- No forced hype.
- No guaranteed returns or profit claims.
- No price prediction or promise of future value.
- Open and consistent communication.
- Public documentation of material actions.
- Respect for uncertainty and responsible correction of errors.
- Long-term stewardship over short-term manipulation.

The project should distinguish official information from community speculation and should clearly label speculation, proposals, and completed actions.

## 17. Disclaimers

Legacy6Coin is a digital asset project. Nothing in this whitepaper constitutes financial, investment, legal, or tax advice or a promise of profit.

Holding or interacting with L6C is undertaken at the participant’s own risk. Nothing states or implies that L6C has, or will have, a particular market value, liquidity, listing, utility, or demand.

Contract source verification, documentation, and testnet deployment provide evidence for review but do not guarantee security or outcomes.

## 18. Conclusion

Legacy6Coin is an attempt to build a transparent narrative around resilience without converting uncertainty into hype. The project has moved beyond its original narrative foundation to a documented Sepolia deployment, but it remains in an early, testnet, and review-oriented phase.

Its standard is not to claim certainty, but to preserve the record: deployment facts, allocation limits, governance authority, treasury constraints, recovery assumptions, testing obligations, and known risks.

**Legacy 6 Coin (L6C) — Built for the world, documented before expansion.**

**Founder:** Michael Wamai Maina Gatane

**Founder statement:** “Scars that sing. Echoes that remain. Legacy that walks forward.”
