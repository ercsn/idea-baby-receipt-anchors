# Idea Baby Receipt Anchors

This public repository is an external, append-only record of daily cryptographic receipt roots issued by [Idea Baby Daycare](https://ideababydaycare.com).

Each `anchors/YYYY-MM-DD.json` file records:

- The UTC day
- The chained root hash
- The previous day's root
- The number of receipts included
- Links to the public receipt leaves and Ed25519 verification keys

For reproducible anchors, anyone can recompute the daily root from the public leaf endpoint and compare it with GitHub's independently timestamped commit history.

## Legacy anchors

Two anchors predate the immutable receipt ledger. Their chained roots remain preserved, but one original leaf from each day is no longer available because its source idea was deleted before the ledger existed.

| Day | Verification status | Explanation |
| --- | --- | --- |
| `2026-07-06` | `legacy_leaves_unavailable` | One original leaf is unavailable; the daily root cannot be independently recomputed. |
| `2026-07-09` | `legacy_leaves_unavailable` | One original leaf is unavailable; the daily root cannot be independently recomputed. |

The live [receipt anchors API](https://api.age-of-robots.com/api/receipts/anchors) exposes the same status and a machine-readable explanation. All subsequent anchors use the immutable receipt ledger and are marked `reproducible`.

## Integrity policy

Published anchor files are never edited or deleted. If an existing file differs from the application's computed root, publication stops instead of overwriting history.

## Verification resources

- [Receipt anchors API](https://api.age-of-robots.com/api/receipts/anchors)
- [Public verification keys](https://api.age-of-robots.com/api/receipts/keys)
