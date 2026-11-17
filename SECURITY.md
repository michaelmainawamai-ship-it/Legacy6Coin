# Security Policy

## Security Overview

Legacy6Coin (L6C) is an ERC-20 token implemented by `Legacy6CoinV2`. The project prioritizes transparency, public documentation, source verification, and responsible disclosure. This policy explains the security scope, contract controls, and process for reporting potential vulnerabilities.

The information below describes the published `Legacy6CoinV2` contract and the project deployment status as of the date this policy is published. A source-verified deployment helps reviewers compare the deployed bytecode with its source; it is not, by itself, a guarantee that the contract is free of vulnerabilities or has been independently audited.

## Supported Deployments

| Network | Status | Details |
| --- | --- | --- |
| Sepolia testnet | Deployed; source verified | Chain ID: `11155111`. Contract: [`0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925) |
| Ethereum mainnet | Not deployed | No mainnet contract is currently supported under this policy. A potential mainnet deployment review is targeted for **January 14, 2027**, God willing. This is a review target, not a deployment commitment or authorization. |

Always verify the network and contract address independently before interacting with a token. Testnet assets have no implied mainnet value or equivalence.

## Supported Versions

| Contract / deployment | Security support |
| --- | --- |
| `Legacy6CoinV2` on Sepolia at the address above | Current supported deployment for security reports |
| Mainnet deployment | None; not yet deployed |
| Other contract versions or addresses | Not confirmed as supported; please identify the network, address, and transaction or block details in a report |

The project will update this section if a new deployment or supported version is announced. No other version is implied to be supported by this policy.

## Reporting a Vulnerability

Please report suspected vulnerabilities privately and as soon as possible. **Do not post exploit details, proof-of-concept transactions, or unpatched vulnerability information in public issues, discussions, social media, or other public channels.**

- **Security contact email:** `[SECURITY CONTACT EMAIL — TO BE ADDED]`
- **PGP key / fingerprint:** `[PGP PUBLIC KEY OR FINGERPRINT — TO BE ADDED]`
- **Bug bounty information:** `[BUG BOUNTY PROGRAM OR “NO FORMAL PROGRAM” — TO BE CONFIRMED]`

Until these contact details are published, do not assume that a public repository issue is a confidential reporting channel. The project should publish a monitored private contact method before inviting confidential reports.

Please include, where possible:

- A concise description of the issue and its potential impact.
- The affected network, contract address, and relevant transaction hash or block number.
- The contract version, source or artifact reference, and tools or environment used.
- Reproduction steps or a minimal proof of concept that does not put real users or funds at risk.
- Any suggested mitigation. Please do not include private keys, seed phrases, or other secrets.

## Responsible Disclosure Process

1. **Private report:** Send the details through the published security contact method. If encrypted communication is available, use the published PGP key and verify its fingerprint.
2. **Acknowledgement:** The project aims to acknowledge a report within **3 business days**. If no acknowledgement arrives, follow up through the same private channel; do not disclose the report publicly while waiting.
3. **Triage:** The project will assess severity, affected deployments, exploitability, and potential impact, and will keep the reporter informed as reasonably possible.
4. **Mitigation and coordination:** The project will coordinate remediation or other risk-reduction steps with the reporter. The reported contract may be non-upgradeable, so mitigation could require user guidance or a separately reviewed deployment rather than an in-place contract change.
5. **Disclosure:** The project and reporter will agree on a reasonable disclosure date after users have had an opportunity to understand and respond to the risk. Avoid public disclosure of actionable details before coordinated disclosure.
6. **Credit:** With the reporter’s consent, the project may acknowledge their contribution in a public advisory. Reports are handled in good faith; no reward is guaranteed unless a formal bug bounty program is announced.

Please act in good faith, avoid privacy violations, service disruption, social engineering, and accessing or modifying data that is not yours. Do not move tokens or funds, exploit the issue beyond what is necessary to demonstrate it safely, or test against third-party systems without authorization.

## Security Assumptions

- Users independently verify the network and contract address before sending or accepting tokens.
- The published source and verification refer to the specific Sepolia deployment above; they do not establish the behavior or safety of other addresses.
- The owner’s private key remains secure. Owner actions are authorized by the account holding that key.
- Ethereum, the selected network, wallets, RPC providers, and third-party integrations operate as expected; risks in those systems are outside the contract’s direct control.
- Token holders understand that transfers, minting, and burns are on-chain actions and may be irreversible.
- No independent audit, guarantee of availability, or investment outcome is implied by source verification or this policy.

## Owner Permissions

The owner has privileged administrative permissions in `Legacy6CoinV2`:

- **Mint tokens** to an address, subject to the hard lifetime supply cap.
- **Add a witness**, which records that address and allocates the specified witness amount, also subject to the same cap.
- **Transfer ownership** through a two-step process: nominate a pending owner, who must then accept ownership.

The owner cannot mint beyond the cap through these functions. Ownership is not a witness-based governance system. Protecting the owner key is an important security assumption; compromise could permit unauthorized minting within the remaining capacity and unauthorized witness additions.

## Witness Permissions

Witnesses are recorded participants in a public registry. A witness receives the defined witness allocation when added, but **witness status does not confer ownership, minting authority, or administrative control**. Witnesses cannot change contract permissions merely by being listed as witnesses. The contract does not provide a witness removal or witness governance mechanism.

## Supply Controls

- **Maximum lifetime supply:** `1,000,000 L6C` (`1,000,000 × 10^18` base units).
- **Founder allocation at deployment:** `660,000 L6C`.
- **Witness allocation:** `1,000 L6C` per witness.
- **Initial witnesses:** Six, for an initial combined issuance of `666,000 L6C`.
- **Remaining mint capacity after the initial allocations:** `334,000 L6C`.

The owner can mint only within the hard maximum supply cap. Minting and witness allocations both count toward cumulative `totalMinted`. Tokens burned by holders decrease circulating `totalSupply`, but **burned tokens do not reduce cumulative `totalMinted` and do not increase future minting capacity**. Consequently, burns do not reopen room under the lifetime cap.

## Contract Security Goals

The contract’s design goals include:

- **Fixed maximum supply:** Enforce a hard upper limit on cumulative issuance.
- **Transparent issuance tracking:** Expose supply and minting state, and emit events for relevant allocation and ownership changes.
- **Public source verification:** Make the deployed source available for public review and comparison with the deployed contract.
- **No blacklist functionality:** The contract is not designed with an owner-controlled blacklist.
- **No confiscation mechanism:** The contract does not provide an administrative function to seize or transfer user balances.
- **No upgrade proxy system:** The contract is not designed to use an upgrade proxy through which implementation logic can be replaced.

These are properties of the published contract design and should not be read as a guarantee against vulnerabilities in the contract, compiler, dependencies, deployment process, or surrounding ecosystem.

## Known Risks

- **Privileged owner key:** A compromised owner key can exercise owner permissions, including minting within remaining cap and adding witnesses. Use strong key-management practices.
- **Owner-controlled issuance:** Supply is capped, but additional issuance up to that cap is controlled by the owner. Users should consider this governance and concentration risk.
- **Allocation concentration:** The founder allocation is substantial relative to the cap. Holders should assess ownership distribution and associated market risks independently.
- **Non-upgradeability:** If a defect is found, the deployed contract cannot be patched through a proxy upgrade. A migration or new deployment may be considered, with its own risks and user coordination requirements.
- **Irreversible transactions:** Mistaken transfers and other confirmed on-chain transactions may not be recoverable.
- **External dependencies and infrastructure:** Wallets, exchanges, RPC endpoints, blockchain consensus, and other integrations can fail or be compromised independently of this contract.
- **Market and operational risks:** Token price, liquidity, exchange availability, and project plans are not guaranteed.

## Smart Contract Security Principles

The project aims to:

- Keep contract source, deployment information, and material changes publicly documented.
- Verify source for supported deployments and clearly identify network and address.
- Apply least privilege and make owner-controlled actions and their limits understandable.
- Review changes and deployment artifacts carefully before any future deployment.
- Respond to credible vulnerability reports privately, promptly, and in good faith.
- Avoid describing a source-verified contract as risk-free or implying that verification is equivalent to an independent security audit.

## Disclosure Timeline

The project’s target response timeline is:

| Stage | Target |
| --- | --- |
| Acknowledge a report | Within 3 business days |
| Initial triage and severity assessment | Within 7 calendar days of acknowledgement, where sufficient information is available |
| Status updates | At least every 14 calendar days while the report remains under active review, where practicable |
| Public disclosure | Coordinated with the reporter after mitigation or an agreed response period; timing depends on severity, exploitability, and user risk |

These are response targets, not guarantees. The project may adjust timing when needed to protect users or coordinate remediation, and will communicate material delays to the reporter where possible.

## Disclaimer

Cryptocurrency investments are inherently risky. Token values may fluctuate significantly, and users may lose some or all of their funds. Nothing in this policy is financial, investment, or legal advice, or a guarantee of security, performance, or profit. Users should conduct their own due diligence and consult qualified advisers where appropriate.
