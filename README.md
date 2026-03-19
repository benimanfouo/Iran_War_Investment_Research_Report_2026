# 📊 Iran/Middle East War — Investment Research Report 2026

> A live, self-contained HTML investment research report tracking 40 war-driven stock positions across global markets. Built for analysts, portfolio managers, and informed investors navigating the geopolitical market disruption caused by the 2026 Iran/Middle East conflict.

---

## 🌐 Live Page

Hosted on GitHub Pages:
```
https://<your-username>.github.io/<your-repo-name>/Iran_War_Investment_Research_Report_2026.html
```

> Replace `<your-username>` and `<your-repo-name>` with your actual GitHub username and repository name.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [File Structure](#file-structure)
- [Tech Stack](#tech-stack)
- [SEO & Metadata](#seo--metadata)
- [Favicon](#favicon)
- [How to Update Stock Data](#how-to-update-stock-data)
- [Adding New Stocks](#adding-new-stocks)
- [Macro Signals Panel](#macro-signals-panel)
- [Hosting on GitHub Pages](#hosting-on-github-pages)
- [Research Methodology](#research-methodology)
- [Sources & References](#sources--references)
- [Disclaimer](#disclaimer)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [License](#license)

---

## Overview

This repository contains a single-file HTML investment research report built to track and communicate a **40-stock geopolitical investment strategy** centred on the 2026 Iran/Middle East conflict and its cascading effects on global supply chains, energy markets, defence procurement, and investor sentiment.

The report is designed to:
- Be **read directly in any browser** with no dependencies or server required
- Be **hosted as a static page** on GitHub Pages
- Be **updated over time** as new stock data, analyst commentary, and macro signals evolve
- Be **distributed to clients and analysts** as a standalone HTML attachment or URL link

The strategy is split into two core portfolios:

| Portfolio | Count | Time Horizon | Summary |
|-----------|-------|--------------|---------|
| **SHORT positions** | 20 stocks | Near-term | Companies with direct Gulf exposure, fuel cost vulnerability, or supply chain collapse risk |
| **BUY positions** | 20 stocks | 6–12 months | US energy majors, defence primes, gold miners, domestic food producers, and defence AI |

---

## Features

- **Interactive dashboard** — tabbed interface with sector filters, stock detail panels, and a live sector performance chart
- **40 fully documented stock picks** — each with ticker, exchange, risk rating, full investment thesis, and supporting evidence
- **Macro signals panel** — real-time key indicators (Brent crude, gold, VIX, Hormuz traffic, maritime insurance, Fed rate timeline)
- **Sector performance chart** — horizontal bar chart powered by Chart.js comparing war winners vs losers
- **Print-to-PDF support** — one-click print button with clean print stylesheet
- **Fully responsive** — works on desktop, tablet, and mobile
- **SEO optimised** — meta description, favicon, semantic HTML structure
- **Self-contained** — single `.html` file with all styles and scripts inline (except Chart.js CDN)
- **No framework dependencies** — plain HTML, CSS, and vanilla JavaScript

---

## File Structure

```
/
├── Iran_War_Investment_Research_Report_2026.html   ← Main report file
├── README.md                                        ← This file
└── assets/                                          ← (Optional) Future images or data files
    └── favicon/
        └── web-app-manifest-192x192.png
```

> The report is intentionally built as a **single HTML file** to make it easy to email as an attachment, host as a static page, or open locally without any build step or server.

---

## Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Markup** | HTML5 | Page structure and semantic layout |
| **Styling** | Vanilla CSS3 | All layout, typography, colour, print styles |
| **Interactivity** | Vanilla JavaScript (ES6) | Tab switching, stock detail panels, chart rendering |
| **Charts** | [Chart.js 4.4.1](https://www.chartjs.org/) via CDN | Sector performance horizontal bar chart |
| **CDN** | [cdnjs.cloudflare.com](https://cdnjs.cloudflare.com) | Chart.js script delivery |
| **Hosting** | GitHub Pages | Static file hosting |
| **Favicon** | PNG 192×192 | Hosted on Backblaze B2 S3-compatible storage |
| **Version control** | Git / GitHub | Source control and deployment |

### Why no framework?

The report is intentionally built without React, Vue, or any JavaScript framework. The reasons are:

1. **Portability** — a single `.html` file can be emailed, opened offline, or hosted anywhere
2. **Zero build step** — no `npm install`, no webpack, no compilation required
3. **Longevity** — plain HTML/CSS/JS will render correctly in any browser, now and in the future
4. **Client distribution** — analysts and clients can open it directly without installing anything

---

## SEO & Metadata

The following meta tags are included in the `<head>` of the HTML file:

```html
<!-- Character encoding -->
<meta charset="UTF-8">

<!-- SEO meta description -->
<meta name="description" content="Iran & Middle East War Investment Research Report 2026 — 40-stock strategy identifying 20 stocks to short and 20 to buy across energy, defence, gold, logistics and food sectors. Cross-referenced from 15+ institutional sources including J.P. Morgan, Bloomberg and Deloitte. March 2026.">

<!-- Favicon (standard browser tab) -->
<link rel="icon" type="image/png" href="https://atlas-network.s3.us-west-004.backblazeb2.com/falcon-spears/images/favicon/web-app-manifest-192x192.png">

<!-- Apple home screen icon -->
<link rel="apple-touch-icon" href="https://atlas-network.s3.us-west-004.backblazeb2.com/falcon-spears/images/favicon/web-app-manifest-192x192.png">

<!-- Web app manifest icon -->
<link rel="manifest" href="https://atlas-network.s3.us-west-004.backblazeb2.com/falcon-spears/images/favicon/web-app-manifest-192x192.png">

<!-- Page title -->
<title>Iran/Middle East War — Investment Research Report 2026</title>
```

### Recommended additions (optional)

If you plan to share the page on LinkedIn, Twitter/X, or in Slack previews, add these Open Graph tags directly below the meta description:

```html
<meta property="og:title" content="Iran/Middle East War — Investment Research Report 2026">
<meta property="og:description" content="40-stock geopolitical investment strategy — 20 shorts and 20 buys across energy, defence, gold, logistics and food. March 2026.">
<meta property="og:type" content="article">
<meta property="og:url" content="https://<your-username>.github.io/<your-repo-name>/Iran_War_Investment_Research_Report_2026.html">
<meta property="og:image" content="https://atlas-network.s3.us-west-004.backblazeb2.com/falcon-spears/images/favicon/web-app-manifest-192x192.png">
```

---

## Favicon

The favicon is served from Backblaze B2 cloud storage at:

```
https://atlas-network.s3.us-west-004.backblazeb2.com/falcon-spears/images/favicon/web-app-manifest-192x192.png
```

**Specifications:**
- Format: PNG
- Dimensions: 192 × 192 pixels
- Use: Browser tab icon, Apple home screen icon, web app manifest icon

> If you ever change the favicon, update all three `<link>` tags in the `<head>` section of the HTML file to point to the new URL.

---

## How to Update Stock Data

As market conditions evolve, you will want to update prices, performance figures, and investment theses. All stock data lives in the HTML file as inline JavaScript strings and HTML content.

### Step 1 — Open the file

Open `Iran_War_Investment_Research_Report_2026.html` in any code editor (VS Code recommended).

### Step 2 — Find the stock row you want to update

Each stock is written as a `<div class="stock-row">` element with an `onclick` handler containing the stock detail data. For example:

```html
<div class="stock-row" onclick="showDetail('XOM','ExxonMobil','Your updated thesis here...','Sector: US Oil Major · Updated metric here')">
```

### Step 3 — Update the detail string

The `showDetail()` function takes four arguments:

| Argument | What it contains | Example |
|----------|-----------------|---------|
| 1st | Ticker symbol | `'XOM'` |
| 2nd | Company name | `'ExxonMobil'` |
| 3rd | Full investment thesis | `'Jumped 4.7%...'` |
| 4th | Key metrics (separated by ` · `) | `'Sector: US Oil · Down 23%'` |

### Step 4 — Update macro signals

The macro signals panel is in the **Methodology & Signals** tab. Each signal is an HTML row:

```html
<div class="signal-row">
  <span class="signal-dot dot-amber"></span>
  <span class="signal-label">Brent crude price</span>
  <span class="signal-val">Current: ~$104–110/bbl</span>
</div>
```

Update the `signal-val` span with the latest figure. Change `dot-amber` to `dot-green` or `dot-red` to reflect the current signal status.

### Step 5 — Update the sector chart

The chart data array is in the `<script>` block at the bottom of the file:

```javascript
data: [20, 25, 18, 11, 12, -18, -11, -9, -9, -15],
```

Update these numbers to reflect the latest sector performance figures. The order matches the labels array directly above it.

### Step 6 — Update the top metric cards

The four summary cards at the top (Brent Crude, Global Stocks, Gold Price, Hormuz Supply) are plain HTML:

```html
<div class="meta-card danger">
  <div class="label">Brent Crude</div>
  <div class="value">$104–110</div>
  <div class="sub">+48% since conflict (Feb 28)</div>
</div>
```

Update the `.value` and `.sub` text as prices change.

---

## Adding New Stocks

As new investment opportunities emerge, you can add stocks to either the SHORT or BUY sections.

### Template for a new stock row

Copy and paste this template into the appropriate sector panel inside the `<div class="stock-list">` container:

```html
<div class="stock-row" onclick="showDetail(
  'TICKER',
  'Company Full Name',
  'Full investment thesis — explain why this stock belongs in the short or buy list, cite data points, analyst estimates, and key risk factors.',
  'Sector: Sector Name · Risk: High/Med/Low · Key metric 1 · Key metric 2'
)">
  <span class="ticker">TICKER</span>
  <div class="stock-info">
    <div class="name">Company Full Name</div>
    <div class="reason">One-line summary of the thesis</div>
  </div>
  <span class="risk-badge risk-high">HIGH</span>
</div>
```

### Risk badge classes

| Class | Use when |
|-------|----------|
| `risk-high` | Very high conviction short or very strong buy |
| `risk-med` | Moderate risk or supporting position |
| `risk-low` | Low risk, strong buy with visible earnings floor |

### Adding a new sector panel

To add an entirely new sector (e.g. Pharmaceuticals, Real Estate), copy an existing `<div class="panel">` block and update:
- The `<h3>` sector title
- The `badge-short` or `badge-buy` badge
- The stock rows inside `<div class="stock-list">`

---

## Macro Signals Panel

The macro signals panel in the Methodology tab uses three dot colours to indicate signal direction:

| Class | Colour | Meaning |
|-------|--------|---------|
| `dot-green` | Green | Positive / bullish signal |
| `dot-amber` | Amber | Neutral / watch signal |
| `dot-red` | Red | Negative / bearish signal |

Update both the dot class and the value text when conditions change. This gives readers an instant visual read on the current macro environment.

---

## Hosting on GitHub Pages

### Initial setup

1. Push the repository to GitHub
2. Go to your repository → **Settings** → **Pages**
3. Under **Source**, select `Deploy from a branch`
4. Select `main` branch and `/ (root)` folder
5. Click **Save**

GitHub will provide a URL in the format:
```
https://<your-username>.github.io/<your-repo-name>/
```

Your report will be accessible at:
```
https://<your-username>.github.io/<your-repo-name>/Iran_War_Investment_Research_Report_2026.html
```

### Updating the live page

Every time you push a commit to the `main` branch, GitHub Pages automatically rebuilds and redeploys. Updates are typically live within 1–2 minutes.

```bash
# Standard update workflow
git add Iran_War_Investment_Research_Report_2026.html
git commit -m "Update: Brent crude prices and XOM thesis — March 19 2026"
git push origin main
```

### Recommended commit message format

```
Update: [what changed] — [date]

Examples:
Update: Brent crude $118, gold $5,200, added PANW to buys — March 25 2026
Update: Covered AAL short, added delta hedge note — April 2 2026
Update: New sector — Pharmaceuticals (3 shorts added) — April 10 2026
```

---

## Research Methodology

### Short selection criteria

Each short position was selected against five criteria:

1. **Fuel cost sensitivity** — fuel/energy represents 15%+ of operating costs with inadequate hedging
2. **Gulf route dependency** — >10% of capacity or revenue requires Hormuz/Suez/Gulf corridors
3. **Supply chain input vulnerability** — >30% of critical inputs sourced from Gulf region
4. **Insurance/reinsurance war-zone liability** — direct exposure to energy facility or aviation war claims
5. **Consumer demand collapse** — tourism, discretionary, or Gulf-market revenue at risk

### Buy selection criteria

Each buy position was selected against five criteria:

1. **US domestic oil production advantage** — breakeven $35–55/barrel vs Brent $104+
2. **Defence contract backlog** — multi-year sole-source programmes immune to political budget cycles
3. **Gold/safe-haven demand** — structurally elevated by geopolitical risk + central bank buying
4. **US domestic supply chain immunity** — food/fertilizer producers gaining pricing power vs disrupted imports
5. **Revenue model resilience** — MLP pipelines earning on volume; streaming companies with no operational risk; SaaS defence with recurring contracts

### Time horizon

**6–12 months.** Based on Chatham House's "moderate scenario" which projects Brent peaking at ~$130 before declining in H2 2026. Short positions are most compelling in the near term; long positions are strongest 3–9 months out as defence procurement cycles mature and energy earnings upgrades are reflected in consensus estimates.

---

## Sources & References

This report was cross-referenced against the following institutional and financial intelligence sources:

| Source | Publication |
|--------|------------|
| World Economic Forum | Global Risks Report 2026 |
| J.P. Morgan | Global Research — Iran Conflict Market Effects (Mar 2026) |
| Charles Schwab | Investment Research — Iran War Impact on Global Equities (Mar 13, 2026) |
| Deloitte Insights | Iran and Middle East Conflict Impacts Global Economy (Mar 2026) |
| Chatham House | How Will the Iran War Affect the Global Economy? (Mar 2026) |
| Bloomberg Intelligence | Stock Trader's Guide to Supply Disruption (Mar 15, 2026) |
| Bloomberg | Defense to Airlines — How Stocks Are Reacting (Mar 2026) |
| Benzinga | Iran War Hormuz Stock Baskets (Mar 2026) |
| Morningstar | Where to Invest as Iran War Hits Global Markets (Mar 2026) |
| TipRanks | 5 Stocks to Watch in Energy and Defense (Mar 2026) |
| Reuters | How US-Israeli War on Iran Is Upending Global Business (Mar 18, 2026) |
| Al Jazeera | How Badly Has the Iran War Hit the Global Economy (Mar 16, 2026) |
| Motley Fool | Iran War — Pipeline, Defense, Gold Stocks (Mar 2026) |
| DividendInvestor.com | Five Dividend-Paying Energy Stocks (Mar 2026) |
| CSIS | What Does the Iran War Mean for Global Energy Markets? (Mar 2026) |
| TIME Magazine | How the War with Iran Is Impacting Economies in Asia (Mar 16, 2026) |
| GOBankingRates | Iran War Investing — Sectors to Reconsider (Mar 2026) |
| USFunds.com | Oil and Freight Markets Surge as Gulf Conflict Escalates (Mar 2026) |

---

## Disclaimer

> This report is for **informational and educational purposes only**. It does not constitute financial, investment, legal, or tax advice. All investments carry risk, including the possible loss of the entire amount invested. Short selling involves unlimited loss potential and is only appropriate for experienced investors with appropriate risk tolerance and margin accounts. Past performance is not indicative of future results. All data has been compiled from publicly available sources and may not be current at the time of reading. Geopolitical situations are highly unpredictable — a ceasefire, Hormuz reopening, or diplomatic breakthrough could rapidly reverse all war-driven market moves. You should consult a qualified financial advisor before making any investment decisions.

---

## Contributing

This is a living research document. Contributions, corrections, and updates are welcome.

### To suggest a stock addition or correction

1. Open an **Issue** in this repository
2. Use the title format: `[Stock] TICKER — Add / Update / Remove`
3. Include: ticker, exchange, thesis summary, and supporting source links

### To make a direct edit

1. Fork the repository
2. Make your changes to `Iran_War_Investment_Research_Report_2026.html`
3. Open a **Pull Request** with a clear description of what you changed and why
4. Include data sources for any new or updated figures

---

## Roadmap

Planned updates and enhancements as the conflict and market situation evolves:

- [ ] Add Open Graph meta tags for social media sharing previews
- [ ] Add a `Last Updated` timestamp that auto-displays at the top of the page
- [ ] Expand to 30 short / 30 buy positions as new opportunities emerge
- [ ] Add a Pharmaceuticals sector panel (medical supply chain disruption)
- [ ] Add a Real Estate sector panel (Gulf commercial property collapse)
- [ ] Add European defence stocks (Rheinmetall, BAE Systems, Leonardo SpA)
- [ ] Add a ceasefire/de-escalation scenario section with position unwind guidance
- [ ] Add a version history / changelog section to the report HTML
- [ ] Integrate a lightweight JSON data file to separate stock data from presentation code
- [ ] Add a `robots.txt` and `sitemap.xml` for improved SEO indexing

---

## License

This research report and repository are proprietary. All rights reserved.

No part of this report may be reproduced, redistributed, or used for commercial purposes without explicit written permission from the author.

For licensing enquiries, client distribution rights, or white-label use, please contact the repository owner directly.

---

*Last updated: 19 March 2026*
