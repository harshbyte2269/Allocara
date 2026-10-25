# Allocara roadmap

- [x] Extend the page assistant with latest-available NSE/BSE/US stock-price tools and cited finance research; live Indian/US quotes, basic finance, RBI source lookup and missing-symbol handling checked; 163 tests pass. Coverage depends on provider availability, not a guaranteed real-time feed.

- [x] Replace Plain words summary with a site-wide current-page conversational AI assistant; private fields excluded, page numbers and simple wording tested, live homepage/follow-up and entered planning values verified.

- [x] Remove the Crash path card from the homepage analysis tools list; the icon import is gone too.

- [x] Redesign normal/crisis money-versus-risk using real selected-holding history; add refreshable AI insights to both and remove independent bets and correlation sections. Measured attribution and AI request inputs tested; public empty state checked.
- [ ] Verify populated Risk Map and live AI reviews against the requesting user's saved stocks — no matching signed-in account is available; requires their sign-in or choice of test account.

- [x] Ground Overview cards, cash-need outcomes and goal states in entered portfolio data; add authenticated, numerically checked AI holding insights and improve the presentation. All 143 tests pass; public desktop/mobile states checked.
- [ ] Verify Overview and live AI insights against the requesting user's saved holdings — no matching authenticated account is available; requires their sign-in or choice of test account.

- [x] Remove the financial goals section from My Account; a form test guards that the goals fields stay out.

- [x] Remove the Goal Simulation tab, its page and its homepage card; the development engine self-tests now run from the analyser shell instead.


- [x] Remove the month-by-month crash path from Scenario Lab; page checks cover the reverse stress fall, sale pricing from the user's own buy price, and the per-holding what-if.

- [x] Add recorded-value graphs to holding comparison; selection updates tested and graphs browser-checked in isolation at desktop and phone widths. Signed-in saved-portfolio verification remains blocked below.

- [x] Replace portfolio comparison with portfolio selection and distinct holding comparison; selection and actual holding metrics covered by automated tests.
- [ ] Verify holding comparison against a signed-in saved portfolio — requesting user has no matching account; sign-in in the preview is required.

- [x] Replace holdings entry with guided questions and 100 verified Indian stock choices; preserve saved holdings; entry flow tested and browser checked in isolation.
- [ ] Verify guided portfolio saving in a signed-in account — requesting user has no matching account; sign-in is required.

- [x] Add selected planning and research calculators with tested formulas and user-entered data.
- [x] Add private journals, dividends, rules, watchlist, practice portfolios, news exposure, and corporate actions.
- [x] Add tool navigation, source timestamps, monthly report, and stored-data deletion; verify public calculator flows and layouts.
- [ ] Verify private record saving and data clearing end-to-end — waits for the user to sign into the preview; no account matches the requesting user for session restoration.

- [x] Arrange the introduction beside recent Indian market charts and verify the market display.

- [x] Phase 1: design tokens, asset table, engine items 1–7 with tests, landing stub
- [x] Phase 2: engine items 8, 10–15 with tests; analyser layout + left controls + Overview tab
- [x] Phase 3: remaining tabs (Scenario Lab, Risk Map, Goal Simulation, Compare, Assumptions); full landing page
- [x] Phase 4: data pipeline, Past performance tab, measured crisis correlation, bootstrap, quiz
- [x] Phase 5: demo mode, print report, save/load, plain-words summary, polish, accessibility
- [x] Phase 6: compressed shareable links, optional guarded AI explainer, history CSV upload, final tests and README
- [x] Accounts: sign in/sign up, basic profiles, private portfolio and settings autosave, password recovery, unit tests and public-screen checks
- [x] Verify account saving end-to-end with a confirmed account
- [x] Replace sample portfolio defaults with empty setup and account investor/holdings entry; verify saving and analysis.
