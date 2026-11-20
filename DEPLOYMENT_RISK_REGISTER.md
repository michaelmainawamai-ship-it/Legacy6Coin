# Legacy6Coin (L6C) Deployment Risk Register

**Project:** Legacy6Coin (L6C)  
**Founder:** Michael Wamai Maina Gatane  
**Scope:** Project, operational, and potential future mainnet deployment risks

## Purpose

Identifying risks early improves project resilience by making assumptions, controls, and outstanding decisions visible before they affect users or project operations. This register records material known risks and practical mitigations for review. It is a working document, not a guarantee that every risk has been identified or eliminated.

Legacy6Coin's published documentation states that the Sepolia deployment is source-verified and that Ethereum mainnet is not deployed. A review milestone is not authorization or a promise to deploy. Risk assessments below are qualitative and should be updated as evidence, controls, and project circumstances change.

## Risk Categories

- **Smart Contract Risk** — defects, unintended behavior, or deployment and configuration errors in contract code or its dependencies.
- **Wallet Security Risk** — unauthorized access to wallets or signing devices.
- **Key Management Risk** — loss, theft, exposure, or inadequate recovery of private keys and seed phrases.
- **Liquidity Risk** — inadequate, incorrectly configured, or insufficiently disclosed liquidity arrangements.
- **Governance Risk** — concentrated authority, unclear decision processes, or undocumented use of privileged permissions.
- **Documentation Risk** — missing, outdated, inconsistent, or ambiguous project information.
- **Community Risk** — misunderstanding of token supply, allocation, project status, or risks.
- **Regulatory Risk** — changes in or uncertainty about legal and regulatory requirements applicable to the project or its participants.
- **Exchange Listing Risk** — listing decisions, availability, and ongoing support depend on independent third parties and are not assured.
- **Operational Risk** — failures in project processes, records, people, tooling, or service providers.

## Risk Register Table

Likelihood and impact are qualitative assessments for prioritization, not statistical forecasts. Status describes the current documented state of the risk and mitigation; it does not imply that the risk has been resolved.

| Risk ID | Category | Description | Likelihood | Impact | Mitigation | Status |
| --- | --- | --- | --- | --- | --- | --- |
| R-001 | Wallet Security Risk; Governance Risk | If the owner wallet is compromised, an unauthorized party may exercise the contract's owner permissions, including minting within the remaining supply cap, adding witnesses, or initiating ownership transfer. | Medium | Critical | Use a hardware wallet for privileged actions; secure devices and recovery material separately; verify transaction details on-device; minimize hot-wallet exposure; document and disclose material owner actions; review access and wallet security periodically. | Open — owner-key security is a documented assumption; implementation of proposed controls should be verified before deployment. |
| R-002 | Key Management Risk; Operational Risk | Loss of the private key or seed phrase may permanently prevent access to the associated wallet and its privileges or assets. | Medium | High | Maintain encrypted, offline backups in secure, geographically separated locations; restrict access; test the recovery procedure using a non-production wallet; never put seed phrases in repository files, cloud notes, or public communications. | Open — recovery arrangements and a tested procedure require confirmation. |
| R-003 | Smart Contract Risk; Operational Risk | An incorrect network, contract artifact, constructor parameter, deployer account, or deployment transaction could result in an unusable or unintended mainnet deployment. Confirmed on-chain deployments may not be reversible. | Medium | Critical | Pin and review source, compiler, and build settings; independently verify the network, chain ID, address, bytecode, and transaction parameters; test scripts and rehearse the procedure on a test network; use an independent pre-deployment review and post-deployment verification; retain signed-off records. | Open — mainnet is documented as not deployed; deployment controls remain a precondition. |
| R-004 | Liquidity Risk; Operational Risk | Incorrect liquidity amounts, pool selection, paired asset, transaction parameters, or disclosure could result in loss, inaccessible liquidity, or misleading public information. No initial mainnet liquidity allocation is documented as finalized. | Medium | High | Approve a written liquidity allocation and policy before action; verify pool and amounts independently; test transaction steps where possible; record approvals, wallet addresses, transaction hashes, and purpose; disclose actions in the ledger. | Open — initial allocation is not finalized in the published Liquidity Policy. |
| R-005 | Documentation Risk; Community Risk | Conflicting or outdated documentation about supply, allocations, permissions, network status, or deployment plans could mislead readers and reviewers. | Medium | High | Maintain authoritative documents; cross-check figures and terminology across README, security, tokenomics, governance, and liquidity documents; date material revisions; link disclosures to transaction evidence; review documentation before releases. | Open — consistency review is ongoing and should be repeated before material announcements or deployment. |
| R-006 | Community Risk; Documentation Risk | Readers may misunderstand tokenomics, including the 1,000,000 L6C maximum supply, 666,000 L6C initial minted supply, and 334,000 L6C remaining issuable supply, or mistake a target review date for a deployment commitment. | Medium | High | Publish plain-language supply and permission explanations; state that remaining issuable supply is not formally allocated and is not a commitment to issue; label dates as review milestones; make clear that testnet tokens do not imply mainnet value or equivalence. | Open — communications should be checked against the current published tokenomics and security documents. |
| R-007 | Governance Risk; Smart Contract Risk | The contract owner can issue additional tokens up to the hard lifetime cap. The remaining 334,000 L6C is not formally allocated; unclear controls or disclosure could lead to misuse or unexpected issuance. | Medium | High | Document any issuance rationale and approval process before use; disclose amount, recipient, purpose, and transaction reference promptly; maintain an issuance record and reconcile it to on-chain supply; avoid implying that witness status is governance authority. | Open — remaining issuance is not formally allocated; owner-controlled issuance remains a documented contract capability. |
| R-008 | Operational Risk | Underestimating mainnet gas costs or fee volatility may delay deployment, cause failed transactions, or create pressure to use an inadequately reviewed deployment path. | Medium | Medium | Estimate costs using current network conditions; maintain an approved budget and reserve; simulate deployment steps and estimate gas; set transaction fee limits deliberately; do not bypass review to meet a date. | Open — costs and funding should be reassessed immediately before any deployment decision. |
| R-009 | Operational Risk; Governance Risk | Reliance on a single founder for approvals, key access, documentation, and operational decisions creates continuity, availability, and oversight risks. | High | High | Document critical procedures and decision history; identify a secure continuity and succession process; separate treasury and founder wallets; introduce independent review for high-impact actions where feasible; avoid sharing secrets as a workaround. | Open — single-founder dependency is an ongoing structural risk requiring documented continuity planning. |
| R-010 | Operational Risk; Documentation Risk | Loss or corruption of project records, deployment artifacts, approvals, or transaction evidence could impair recovery, auditability, and accurate public disclosure. | Medium | High | Keep version-controlled records in the repository; maintain independent encrypted backups and release archives; record artifact hashes, addresses, chain IDs, and transaction references; periodically test restoration and access. | Open — backup and restoration arrangements require periodic verification. |

## Active Risk Summary

These qualitative levels prioritize attention and do not represent measured probabilities. Risks remain active until mitigations are implemented and their effectiveness is reviewed.

- **Critical:** R-001 owner wallet compromise; R-003 incorrect mainnet deployment.
- **High:** R-002 private key loss; R-004 liquidity misconfiguration; R-005 documentation inconsistency; R-006 community misunderstanding of tokenomics; R-007 unallocated issuance misuse; R-009 single-founder operational dependency; R-010 loss of project records.
- **Medium:** R-008 mainnet gas cost underestimation.
- **Low:** No risks currently rated Low. This means no listed risk has been assessed as low priority; it is not evidence that low-level risks are absent.

## Review Cycle

Review this register at least quarterly and before any future mainnet deployment. Also review it after a material contract, wallet, governance, liquidity, regulatory, or operational change; a security incident; or a material public disclosure. Record the review date, reviewer, changed ratings, evidence considered, and mitigation owners or target dates. Do not mark a risk closed solely because a mitigation is planned.
