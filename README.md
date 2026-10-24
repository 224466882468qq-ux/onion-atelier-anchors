# Onion Atelier Ledger Anchors

This public repository is an independent, append-only checkpoint for the
Onion Atelier gift ledger. It contains no private keys, user secrets, database
files or application source.

Every file under `anchors/` is newline-delimited JSON. A new line is committed
only when the ledger head changes. The Onion service itself remains the source
of the complete ledger; these commits preserve public timestamps of earlier
heads so later history rewrites can be detected.

## Verify an anchor

1. Read the matching `anchors/YYYY-MM-DD.ndjson` commit history.
2. Compare `headHash`, `ledgerSequence`, `records` and
   `publicKeyFingerprint` with `/api/ledger` from the Onion site.
3. Verify every local ledger record and its ECDSA signature in the browser.

GitHub can still remove this repository or rewrite its history. This is one
independent public checkpoint, not a mathematical guarantee of permanence.
Additional repositories in the automation configuration create independent
mirror checkpoints.
