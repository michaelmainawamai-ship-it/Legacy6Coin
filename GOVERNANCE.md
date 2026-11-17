# Legacy6Coin (L6C) Governance and Permissions

This document describes the documented administrative roles of the `Legacy6CoinV2` contract. It is not a claim that the project has decentralized governance or token-holder voting. Always verify current ownership and contract state on the [verified Sepolia contract page](https://sepolia.etherscan.io/address/0xae0F6F5B2E3C2312d9748d7A18642Af041f8b925#code).

## Governance Model

The contract has owner-controlled administrative permissions. L6C holders and witnesses do not gain governance powers merely by holding tokens or being recorded as witnesses. No on-chain holder voting mechanism is documented here. Project announcements or community discussions do not themselves change contract permissions.

## Owner Permissions

The contract owner can:

- **Call `mint()` within `MAX_SUPPLY`.** This permits further issuance up to the maximum supply cap. The owner controls whether remaining issuance is used. This is a material centralized authority and a risk for holders.
- **Call `addWitness()`.** This manages witness designation according to the contract's rules. Witness designation is not a grant of owner or governance powers.
- **Call `transferOwnership()`.** This transfers the owner role and its associated permissions to another address according to the contract's ownership mechanism. A transfer changes who controls the documented owner functions; it does not itself decentralize control.

The current owner should be checked on-chain rather than inferred from the deployer, founder identity, or historical documentation. Review the contract's verified source and current read-only state for exact function behavior and role status.

## Witness Permissions and Limitations

Witnesses may receive their witness allocation, and witness addresses are publicly recorded on-chain according to the contract's rules. Witnesses have no ownership or governance powers by virtue of that status.

Witnesses **cannot**:

- mint tokens;
- transfer ownership;
- freeze accounts;
- modify the supply cap or supply; or
- change account balances.

Witness status is not a security certification or endorsement. Witnesses do not approve transactions on behalf of holders.

## Minting and Supply Controls

The maximum supply is 1,000,000 L6C. The initial minted supply is stated as 666,000 L6C, leaving 334,000 L6C of issuance headroom. Minting is owner-controlled and must remain within `MAX_SUPPLY`. The cap limits cumulative issuance; it does not remove the owner's discretion to issue some or all of the remaining headroom.

The contract's documented cumulative issuance tracking means burns reduce `totalSupply` but do not restore `totalMinted` headroom. See [TOKENOMICS.md](TOKENOMICS.md) for supply and burn details.

## Ownership Transfer and Accountability

Ownership transfer is a consequential administrative action. Any transfer should be publicly disclosed with the effective transaction hash, new owner address, and a clear statement of which permissions move. The on-chain record is authoritative for whether a transfer occurred. This disclosure expectation does not add a contract-enforced approval process or multisignature requirement.

## Governance Limitations and Risks

This permission model is not decentralized governance. The owner has privileged authority over minting within the cap, witness administration, and ownership transfer. A compromised, unavailable, or malicious owner key could create operational risk. No claim is made here that the owner uses a multisignature wallet, timelock, or independent approval process unless such controls are separately documented and verifiable.

Future governance proposals must distinguish between discussion, project policy, and changes actually enforced by the contract. Any claim that permissions have changed should be supported by verified source and on-chain evidence.
