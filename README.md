# Interview Prep — Hong Kong Financial Services

One site, one GitHub Pages link, everything reachable from a single home page.

## Structure

- `index.html` — the hub. Lists everything below as cards. **This is what loads at your root URL.**
- `insurance.html` — Insurance industry landscape (reusable across any insurance interview)
- `bank.html` — Banking industry landscape (reusable across any banking interview)
- `role-fidelity-international-po-multi-asset.html` — Fidelity International (FIL), Product Owner, Multi-Asset, Hong Kong
- `role-mirae-asset-ba-lead.html` — Mirae Asset Securities (HK), Business Analyst Lead, retail mobile trading app
- `role-bochk-senior-ba-pm-derivatives.html` — Bank of China (Hong Kong), Senior BA/PM, Financial Derivatives, Treasury & Global Markets Middle Office
- `role-aia-manager-innovation-change.html` — AIA, Manager Innovation Change Management

Two categories, on purpose:

- **Industry landscapes** (`insurance.html`, `bank.html`) share one neutral design system and a pill-switcher at the top of each ("← All prep · Insurance · Banking") since they're reused across many interviews in that sector. When you learn something new about an industry, these get updated in place rather than duplicated.
- **Role-specific prep** (`role-*.html`) is one page per job application, each free to keep its own look (Fidelity International red/blue, AIA red/gold, BOCHK red/gold, Mirae Asset navy/teal) since it's a one-off built for that specific interview, using that company's real brand colours. Each gets a small "← All prep" breadcrumb link at the top so you can always get back to the hub.

## What's in each role page

| Page | Focus |
|---|---|
| **Fidelity International — Product Owner, Multi-Asset** | Multi-Asset, Systematic & Solutions Value Stream, Hong Kong — the steepest domain stretch in this folder. SAFe/Agile Release Train vocabulary vs. Scrum certs, what "multi-asset investing" actually means vs. the retail multi-asset app, the FIL-vs-Fidelity-Investments mix-up, an honest fit map with real gaps in the essential requirements, standardised four-beat self-intro, Q&A, questions to ask. |
| **Mirae Asset — BA Lead** | Identifies the app as **MAPS** (launched late June 2026) and builds everything around a team six weeks post-launch. Standardised four-beat self-introduction. Fit map. Product administration setup (fee groups, user-to-exchange matrix, trading currency, mid FX rate, product whitelist/blacklist mapped to generic terms). SFC internet-trading security, suitability and complex-product rules. Hong Kong's retail virtual asset regime. A **proposed AI wealth-management roadmap** phased by regulatory cost. The **four markets** (HK, Mainland China via Stock Connect, Korea, US) with a rules table and an upcoming-changes table. A **Korean market** section — index performance, notable stocks incl. SK Square, Value-up and Commercial Act reform, and the MSCI omnibus-account angle. Mobile release management. Leading a BA team. Vendors and the Hong Kong–Seoul dynamic. Honest gap read. Q&A. 17 questions to ask. |
| **BOCHK — Senior BA/PM** | OTC FX and derivatives mechanics, an NDF deep-dive with a worked example, Bloomberg-to-Treasury-system connectivity flow, HKTR and the OTC derivatives reporting regime, Murex/Calypso/Summit primer, honest gap framing. |
| **AIA — Manager, Innovation Change Management** | Group Innovation Office, regional scope: fit map, self-intro script, AI use cases relevant to AIA, questions for the panel. |

## Publish on GitHub Pages

1. Create a new GitHub repo (public, so Pages is free).
2. Upload all files in this folder to the **repo root**, flat — no subfolders.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main, folder: / (root) → Save**.
4. You get a URL like `https://<your-username>.github.io/<repo-name>/` within a minute or two — that's your hub page.

### Important: keep every HTML file at the repo root

New files written into the Claude project land under a `claude/` prefix (e.g. `claude/role-mirae-asset-ba-lead.html`), while existing files are updated in place. That prefix only affects how the file is stored in the project — **when you upload to GitHub, every HTML file goes in the repo root**, or the relative links between the hub and the role pages will break.

## Adding a new role-specific prep page later

1. Save the new page as `role-<company>-<short-title>.html` (e.g. `role-manulife-product-manager.html`) — keeps them sorted together and easy to spot in the file list.
2. Read the company's real brand colours off its logo (not an automated brand-colour tool) and build the page's palette around them.
3. Use the standardised four-beat self-intro template (see `claude/tracy-profile-facts.md` in the project) and the fixed section order: self-intro, Q&A, questions to ask, "read this first" (if any), then the rest ordered by whatever makes sense for that role.
4. Add a small "← All prep" breadcrumb link near the top of that page, in whatever style matches its own design (ask Claude — it's a two-line change).
5. Add one card to `index.html`'s "Role-specific prep" section, linking to the new file. **Newest role goes first.**
6. Push both the new file and the updated `index.html`.

No need to touch `insurance.html` or `bank.html` when adding a role-specific page — they're independent.

## Conventions worth keeping

**Confidence marking.** Every substantive claim is tagged:

- **confirmed** — sourced to a primary or company document
- **inference** — a reasoned conclusion from public facts, not a stated fact
- **unverified** — could not be confirmed; do not assert it in an interview

Regulatory paragraph numbers are deliberately omitted wherever the exact citation couldn't be verified. Citing a sub-paragraph wrongly is worse than not citing one at all.

**Adversarial fact-check.** Every role page goes through a dedicated fact-checking pass before delivery — the Mirae Asset page's first draft had 18 issues caught this way (a launch date reported four different ways, two quotations that traced to journalists rather than the company, a Northbound pre-trade-checking rule that was actually the Southbound rule, and a material regulatory circular the first draft missed entirely); the Fidelity International page's pass caught 6, including a backwards claim about JD requirement ordering and several spliced company-values quotes. Worth requesting the same treatment on future pages: it's the difference between a page that sounds well-researched and one you can safely quote from under pressure.

**Standardised self-introduction (locked August 2026).** Every role page now uses the same four-beat template — fixed Beat 1 (who I am) and Beat 2 (current AI-adoption role at FXCM) text with marked swaps, three fixed-theme Beat 3 points (closest project experience; MNC/cross-timezone stakeholder management; independent high-accuracy delivery) rendered as boxed cards, and a fixed close with no gap-hedging. Full template lives in `claude/tracy-profile-facts.md` in the project.

## Time-sensitive content — check before each interview

Some content on the Mirae Asset page dates quickly:

- **Korean index levels.** KOSPI fell roughly 40% and then posted its largest one-day gain on record inside a fortnight in July 2026. Check the current level the morning of the interview — quoting a stale number to a Korean brokerage would undo the credit the section earns.
- **Regulatory items in flight.** The SFC's July 2026 phishing-resistant authentication circular (OTP phase-out by July 2027), the US overnight-session go-live targeted at 6 December 2026, the proposed rescission of SEC Rule 611, HKEX's indicative Q4 2027 T+1 date, and the status of Hong Kong's virtual-asset dealing legislation are all moving. Re-check anything you plan to state as current.

## Note on the Interactive Brokers (IBKR) prep page

A prep page for an Interactive Brokers role (`role-ibkr-sr-pm-bd-apac.html`) was drafted but hasn't been published here — no feedback on that application yet, so it's being held back. If that changes, publish it like any new role-specific page and add its card to `index.html`.

## Note on the DBS prep page

A prep page for a DBS Bank role (`role-dbs-vp-avp-ba-cbg-tno.html`) was previously listed here but has been removed from the hub and this README — that application didn't reach interview stage. The file itself was never stored in this project; if it's still on GitHub, it's now an orphaned page with no card pointing to it.
