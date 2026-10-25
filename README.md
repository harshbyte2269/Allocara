# Allocara

Educational portfolio stress testing for Indian investors. Results are hypothetical ranges, never forecasts or financial advice.

## Analysis and sharing

The analyser includes Overview, Scenario Lab, Risk Map, Compare, Past performance, editable assumptions, a guided demo and a printable report.

Save/load uses this browser's storage; JSON exports transfer full settings. Copy shareable link compresses settings into the URL fragment and restores both portfolios, situation, goals, shocks and return overrides. Anyone with the link can read the settings; compression is not encryption. Uploaded history is not saved, exported or shared.

## Monthly history uploads

Past performance → Upload history CSV replaces bundled history for statistics, measured crisis correlations and bootstrap during the current session. Restore bundled history reverses it. Uploads stay in browser memory and are not sent to Cloud.

Columns: `date` and one or more of `LC,MC,GS,CB,GD,CA,US,LK`. Download the sample from the page. Dates must be unique, oldest-first `YYYY-MM` or `YYYY-MM-01`; at least 12 rows, maximum file size 1 MB. Returns are decimals: `0.02` means 2%; blank cells mean missing data. Unknown columns, malformed rows and losses below −100% are rejected. Bootstrap needs at least 24 rows. Incomplete histories are reweighted over available holdings and can distort results. Sources and caveats: `data/SOURCES.md`.

## Optional AI

Plain-words summary always uses an offline calculated template. When the explanation service is reachable, Explain with AI sends only computed numeric results: no goal names, uploaded history or personal free text. Lovable Cloud hosts the TanStack server function; `@lovable.dev/ai-gateway` reads its managed server credential. Never put private keys in browser configuration. AI usage is metered.

The prompt prohibits arithmetic, trading advice and invented figures. Every numeric token must occur in the submitted results. Unverified, refused or failed replies fall back to the template. This conservative check does not prove all prose is accurate.

## Hosting and offline limits

The platform uses TanStack file routing and its hosted server runtime, not the brief's hash router or standalone static deployment. URL fragments are used only for shared settings. `npm run build` targets the configured TanStack host. Calculations run in the browser and need no AI service once assets are loaded. No service-worker offline installation is provided; fresh offline page loads are not guaranteed. Only optional AI requires Cloud.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
npm run test
```

## Built with

- TanStack Start
- TypeScript
- React
- Tailwind CSS
