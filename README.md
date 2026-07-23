# Idea Baby Receipt Anchors

This public repository is an external, append-only record of daily cryptographic receipt roots issued by [Idea Baby Daycare](https://ideababydaycare.com).

Each `anchors/YYYY-MM-DD.json` file records:

- The UTC day
- The chained root hash
- The previous day's root
- The number of receipts included
- Links to the public receipt leaves and Ed25519 verification keys

Anyone can recompute a daily root from the public leaf endpoint and compare it with GitHub's independently timestamped commit history.

## Integrity policy

Published anchor files are never edited or deleted. If an existing file differs from the application's computed root, publication stops instead of overwriting history.

## Verification resources

- [Receipt anchors API](https://api.age-of-robots.com/api/receipts/anchors)
- [Public verification keys](https://api.age-of-robots.com/api/receipts/keys)
