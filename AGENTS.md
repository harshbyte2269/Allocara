<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Allocara rules
- Holding comparison uses a pure engine for same-portfolio selection and recorded holding metrics; its table and graphs consume the same metrics, with no asset-class assumptions substituted for stock-specific results — prevents misleading or inconsistent holding comparisons.
- Guided holding entry uses the official Nifty 100 snapshot and stores optional NSE symbols in private settings; stock current values come from live NSE quotes fetched server-side (manual entry only when a quote fails) while purchase price stays user-entered — avoids ambiguous names and invented prices while preserving legacy holdings.
- Investment tools use pure user-input engines and owner-scoped tool records; practice positions stay separate from real portfolios, and news embeds never supply calculation prices — avoids invented data and account leakage.
- Stored-data clearing runs atomically as an authenticated security-invoker database function with owner RLS, leaving the sign-in account intact — prevents partial or cross-user deletion.
- Homepage market quotes use a browser-mounted TradingView embed, isolated from portfolio calculations; no synthetic price fallback is shown.
- Engine logic lives in src/engine/* as pure TypeScript with unit tests next to it; no UI imports there — keeps formulas testable and visible.
- Routing uses TanStack Router (platform-fixed) instead of the spec's hash routing — the template does not support swapping routers.
- Colours come only from the CSS variables in src/styles.css; fonts are self-hosted via @fontsource so the app works offline.
- Sharing compresses validated settings into the URL fragment, with no uploaded history included — keeps sharing independent of stored accounts.
- User CSV history replaces the bundled history only in memory and feeds every history consumer — avoids persisting private uploaded data.
- AI explanations use a server-only Lovable Gateway call with computed numeric results and a number-verification fallback — keeps keys and personal text out of requests.
- Plain-words assistance is root-mounted with ephemeral page/identity-scoped conversations; page facts come from fresh privacy-filtered visible content, latest prices from bounded server quote tools, and current finance facts from cited native web research; verified final numbers and deterministic timestamped quote displays keep external facts separate from saved calculations.
- Account state is owned by one root auth subscriber; private profiles and portfolio settings use owner-scoped browser queries with database RLS, and analyser providers are keyed by identity — prevents cross-account state leakage.
- Account autosave waits for saved-state hydration, serializes writes, and never stores uploaded history; shared URLs take initial precedence without overwriting an account until edited — prevents default-state and shared-link overwrites.
- Investor holdings are stored inside validated private account settings and aggregated by asset type for analysis; investor identity and holding names are excluded from shared links — keeps entered holdings authoritative and personal details private.
- Overview derives metrics from the selected recorded holdings, separates held cash from gross listed-stock sale capacity, and requires explicit return inputs for goal projections; its authenticated AI explains symbol-only computed facts with numeric verification — prevents stale aggregates, invented stock returns and ungrounded trading claims.
- Risk Map measures signed covariance contributions from aligned consecutive monthly prices of selected stock symbols (uploads override fetched history); full-history baseline needs 12 returns and worst-negative-decile stress needs six observations, with no class covariance fallback and separately authenticated verified AI reviews — avoids fabricated risk estimates when coverage is insufficient.
