# RestoreLab runbook CLI

Generate reviewable Markdown from a saved inventory, or capture the current public testnet entries in a manifest and assess them. No key file, secret argument or signing feature exists.

```sh
node restorelab-cli/index.mjs plan inventory.json recovery.md
node restorelab-cli/index.mjs inspect restorelab-backend/specimen-manifest.json current-recovery.md
```

Run from the parent of sibling clones. Node 24+. The output is created exclusively: an existing file is not overwritten. The Markdown includes the inventory hash, ledger context, dependency order and scope warning. It is a human runbook, not executable shell or a prepared transaction. Imported labels and evidence are untrusted text; review before sharing. Tests assert ordered prerequisites and the no-transaction disclosure.

## Reference

[Stellar state archival](https://developers.stellar.org/docs/learn/fundamentals/contract-development/storage/state-archival) · [RPC live entry lookup](https://developers.stellar.org/docs/data/apis/rpc/api-reference/methods/getLedgerEntries)
