# Legacy6Coin Asset Archive

This document describes the intended preservation and distribution record for official Legacy6Coin (L6C) branding assets. Its purpose is to support authenticity, attribution, and continuity across repository changes and future archival systems.

## Preservation Locations

Official branding assets are intended to be preserved in the following locations:

- **GitHub repository:** the project’s canonical, version-controlled documentation and asset location. Repository history provides a record of changes over time.
- **Release archives:** published project releases should include the approved assets or a clearly identified branding package, with version and provenance information where available.
- **Future IPFS archives:** assets may be preserved through IPFS. Content identifiers (CIDs) should be recorded in repository documentation after upload and verification.

The presence of an asset in one location should not be assumed to prove that it is present or current in another. Copies should be checked against their documented source or recorded checksum/CID where available.

## Approved Asset References

The approved filenames are recorded in [BRANDING.md](BRANDING.md):

- `assets/L6C-Sigil.png`
- `assets/L6C-Sigil.jpg`
- `assets/L6C-Logo.svg`

When packaging assets, retain these filenames where practical and include relevant source, export, date, and revision details. If an asset is replaced or revised, document the change rather than silently substituting a new file under the same name.

## Community Mirroring

Community members may mirror or redistribute official Legacy6Coin branding assets to support access and preservation. Mirrors should:

- Preserve the asset’s integrity and avoid undocumented edits.
- Preserve attribution to Legacy6Coin.
- Identify the source repository and the date or revision mirrored when known.
- Distinguish the official source asset from local derivatives or format conversions.
- Keep any recorded checksums or IPFS CIDs associated with the exact files they identify.

Mirroring does not make a modified derivative an official asset. Any proposed variants should be clearly labeled and documented separately.

## Archive Maintenance

Contributors maintaining the archive should record material changes in version control, review links and CIDs periodically, and avoid claiming that an item is permanently available unless its availability has been checked. The repository documentation is the human-readable provenance index; external mirrors and distributed archives provide additional preservation paths, not substitutes for clear attribution.

See [IPFS_PRESERVATION_PLAN.md](IPFS_PRESERVATION_PLAN.md) for the staged IPFS workflow.
