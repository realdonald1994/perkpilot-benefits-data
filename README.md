# perkpilot-benefits-data
Public credit card benefits catalog for PerkPilot

## Publication status

Prepared locally for review. No publication is implied. Push and GitHub Pages activation require the repository owner's approval.

## Contents

- manifest.json: catalog release version, timestamp, relative data URL and SHA-256 checksum.
- catalogs/catalog-v1.json: immutable UTF-8 product and benefit definitions.
- CHANGELOG.md: catalog release notes.
- .nojekyll: serve static files without a Jekyll build.
- .gitattributes: preserve LF file bytes across Windows checkouts.
- .gitignore: exclude credentials, personal backups and App workspace files.

Only public definitions belong here. Never add App source, user cards, usage events, personal backups, credentials, API keys or tokens.

## Initial coverage

Version 1 contains two products and three benefits:

| Country | Product | Included benefit | Reset |
| --- | --- | --- | --- |
| CA | American Express The Platinum Card | CAD 200 travel credit | Card membership anniversary |
| CA | American Express The Platinum Card | CAD 200 dining credit; enrollment required | Calendar year |
| US | American Express Gold Card | USD 10 dining credit; enrollment required | Calendar month |

This is a partial benefit list, not a complete statement of card benefits or proof of individual eligibility. Original conditions, sources and verification dates remain in the JSON. lastVerifiedOn remains 2026-10-21; packaging does not invent a newer verification date. Unknown issuer effective dates remain null.

Official sources:

- https://www.americanexpress.com/en-ca/benefits/travel/the-platinum-card/
- https://www.americanexpress.com/en-ca/benefits/the-platinum-card/
- https://www.americanexpress.com/en-us/account/get-started/gold/explore-benefits

## GitHub Pages project URLs

Expected after an approved deployment:

- Manifest: https://realdonald1994.github.io/perkpilot-benefits-data/manifest.json
- Data: https://realdonald1994.github.io/perkpilot-benefits-data/catalogs/catalog-v1.json

The relative dataUrl is catalogs/catalog-v1.json. Resolve it against the Manifest URL to retain the /perkpilot-benefits-data/ project prefix. Do not resolve it against the domain root.

After approval, configure Settings > Pages > Build and deployment > Deploy from a branch: main, / (root). No custom domain or private GitHub token is required in the client. Pages settings have not been changed during preparation.

## Integrity and future releases

Version 1 SHA-256: aa864cbad49065a6560bd51bf155eba79f1f36945b268b3376f9391b2485d815

This checksum covers the exact UTF-8 bytes, including LF newlines and whitespace. Do not edit or reformat an existing release. SHA-256 confirms agreement with the Manifest, not a digital signature or independent issuer verification.

Review official terms, region, dates and eligibility before each new release. Keep stable IDs and old data files, increment the version, and document actual changes. Upload a new immutable data file first and update the Manifest last. Retired definitions keep their identities and history. Never invent terms or publish examples as verified benefits.
