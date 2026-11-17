# Legacy6Coin (L6C)

Legacy6Coin is a founder-led digital asset project centered on resilience, transparency, and responsible stewardship. This repository is the project's public source of truth for contract references, project policies, and documentation. It does not make claims about future price, returns, or outcomes.

## Vision

To build a project whose record is understandable and reviewable: clear about its history, supply controls, risks, and decisions.

## Mission

Legacy6Coin's mission is to foster a community around resilience and transparency, and to document the project's development and stewardship responsibly.

## Legacy Story

Legacy6Coin was created during a period of pressure and uncertainty. Its name reflects the idea that resilience is demonstrated by how people respond to difficulty, and that a meaningful legacy is built through consistent actions over time. This story is context for the project, not a promise of financial or other outcomes.

## Verification Status

`Legacy6CoinV2` has been successfully source verified on the Sepolia test network. The matching bytecode and ABI were generated during verification, and the contract source is publicly viewable.

- **Network:** Sepolia (chain ID 11155111)
- **Contract:** [`0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925`](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code)
- **Deployment transaction:** [`0x8a3bc2c2c8a6b24d477845771c81bc125af4b69fee89ae28fff58141e2e812a7`](https://sepolia.etherscan.io/tx/0x8a3bc2c2c8a6b24d477845771c81bc125af4b69fee89ae28fff58141e2e812a7)
- **Compiler:** Solidity `v0.8.31+commit.fd3a2265`
- **Optimizer:** enabled, 200 runs
- **EVM target:** Paris

This verification applies to the Sepolia deployment only. It is not a security audit, endorsement, or authorization for a mainnet deployment. Sepolia is a test network; this repository does not represent that L6C is deployed on mainnet.

## Supply at a Glance

- **Maximum supply cap:** 1,000,000 L6C
- **Initial minted supply:** 666,000 L6C
- **Remaining lifetime issuance headroom:** 334,000 L6C

The owner controls whether any remaining issuance is minted, subject to the contract's maximum supply cap. Burns reduce the circulating `totalSupply` but do not restore lifetime issuance headroom where cumulative minted supply is tracked. See [TOKENOMICS.md](TOKENOMICS.md) and [GOVERNANCE.md](GOVERNANCE.md) for details.

## Roadmap

The roadmap progresses from documentation, security review, and community formation toward mainnet-readiness assessment. **January 14, 2027 (God willing) is a target review milestone, not a guaranteed deployment date.** See [ROADMAP.md](ROADMAP.md).

## Community

This repository is the current public project documentation channel. Additional official community channels will be listed here when established and verified. Please treat links not published in this repository as unverified.

## Documentation

- [Security policy](SECURITY.md)
- [Tokenomics](TOKENOMICS.md)
- [Liquidity policy](LIQUIDITY_POLICY.md)
- [Roadmap](ROADMAP.md)
- [Governance and permissions](GOVERNANCE.md)
- [Frequently asked questions](FAQ.md)
- [Letter from the founder](LETTER_FROM_THE_FOUNDER.md)
- [Historical verification notes](AUDIT_NOTES.md)

## Disclaimer

L6C is a digital asset and may involve substantial risk, including loss of value, limited liquidity, technical failures, and regulatory uncertainty. Nothing in this repository is financial, investment, legal, or tax advice, an offer, or a promise of profit or future value. No outcome is guaranteed. Readers should independently review the contract, documentation, and applicable risks and laws before interacting with any token or contract.
