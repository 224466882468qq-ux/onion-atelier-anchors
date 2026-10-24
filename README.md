# Onion Atelier Ledger Anchors

This public repository is an independent checkpoint for the Onion Atelier gift
ledger. It contains no private keys, user secrets, databases or app source.

Each `anchors/YYYY-MM-DD.ndjson` line records the public head, sequence,
record count, signer fingerprint and UTC anchor time. A line is committed only
when the ledger head changes.

Compare these values with `/api/ledger` from the Onion site and verify the
complete ledger and ECDSA signatures in the browser. GitHub can still rewrite
history; this is a public checkpoint, not absolute immutability.
