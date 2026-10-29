# S01E03 — what it shows

The signed analysis is at `src/routes/kb/decisions/0002-dedupe-by-cause/+page.svx`.
Its rendered copy is `build/kb/decisions/0002-dedupe-by-cause/index.html`.
The complete static site, including its assets, is in `build/`.

## Reproduce

Use Node.js 22 or newer. Run `npm ci`, then `npm run build`.
Run `npm run preview -- --port 4173` and open
`http://127.0.0.1:4173/kb/decisions/0002-dedupe-by-cause/`.
On machines with an enterprise root certificate installed in the OS, Node may need
`NODE_USE_SYSTEM_CA=1` to use that trust store for package downloads.

The original KB code and datasets are retained. The accepted decision 0001 is unchanged;
0002 proposes its replacement. Report counts, cause attribution, receipt/merge timeline,
and the desk signature stamp are rendered by the original KB components.

The two GitHub issues separate the shared parser (379 unique reports) from the booking-v3
hint (33 unique reports). Intake tags give different counts and are not root-cause evidence.
There are 427 export rows and 412 unique IDs. No product fix is claimed to have shipped.
