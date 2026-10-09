# sc-brrr results

Scored challenge entries for [sc-brrr](https://github.com/btraven00/sc-brrr): one commit per scored
version, written by `score.py` on the scoring host. The scoreboard (`index.html`, data in
`scoreboard.json`) is served by GitHub Pages and rebuilt with `scoreboard.py`.

Layout: `<account>/<name>/<X.Y.Z>/<plan>/<host>/<size>/`, where `<plan>` is the first 8 hex of ob's
`summary_hash()` of the benchmark plan the entry ran in and `<host>` the first 8 hex of
sha256(hostname, CPU model, kernel) of the scoring machine. Each holds the submission and its env,
the exact plan, the runner's `manifest.json` (versions, limits, host facts, data hashes, per-job
exit / OOM / timeout / memory peaks, sha256 of every output), ob's own run metadata
(`ob-metadata/`), `metrics.parquet` and the event and denet traces.

`results.parquet` holds every record of every result in one table; the scoreboard links it.
Outputs themselves are not here, only their hashes.

This repo is a dummy for now: the one entry is the exact reference resubmitted as a test.
