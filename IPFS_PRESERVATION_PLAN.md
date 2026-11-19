# Legacy6Coin IPFS Preservation Plan

This plan describes a staged process for preserving the official Legacy6Coin (L6C) branding assets using IPFS. It emphasizes provenance and verification. IPFS upload, availability, and CID verification must be completed before documentation presents any identifier as established.

## Phase 1 — Prepare and Preserve Source Assets

- Preserve the original JPG as received, without overwriting or recompressing it.
- Export a high-resolution PNG from the preserved source and retain the export details.
- Export an SVG version. Confirm whether it is a faithful vector recreation or a wrapper/trace derived from raster artwork, and document that provenance accurately.
- Keep the approved filenames and identify source files and derivatives clearly.
- Record available metadata, including source, date received, export method, dimensions, and checksums where practical.

## Phase 2 — Upload and Record CIDs

- Upload the approved assets to IPFS using a process that preserves the exact files intended for publication.
- Retrieve and record the CID for each file and for the complete branding package.
- Verify that each CID resolves to the intended content and that retrieved files match the uploaded files.
- Add verified CIDs, upload date, package contents, and any relevant pinning or availability notes to repository documentation.
- Do not replace `[TBD]` values below until upload and verification are complete.

## Phase 3 — Reference Verified CIDs

After verification, reference the appropriate CIDs from:

- `README.md`
- `BRANDING.md`
- `TOKENOMICS.md`

If a referenced document does not yet exist in the repository, add the reference when that document is created. Keep the GitHub repository as the readable provenance record and update all references together when identifiers change or a new package supersedes an earlier one.

## CID Record

**Official Sigil IPFS CID:**  
[TBD]

**Official Logo SVG CID:**  
[TBD]

**Official Branding Package CID:**  
[TBD]

## Verification and Change Control

For each recorded CID, note what exact file or package it identifies. A CID identifies content; it does not by itself guarantee continued availability. Where possible, retain independent copies and periodically check that the content can still be retrieved and matches the documented asset. Record replacements as new versions with new identifiers rather than silently changing the meaning of an existing record.

For broader archival guidance, see [ASSET_ARCHIVE.md](ASSET_ARCHIVE.md) and [BRANDING.md](BRANDING.md).
