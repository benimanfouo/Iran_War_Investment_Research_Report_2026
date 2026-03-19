# Trading Analysis Documentation
## Iran/Middle East War — Advanced Trading Parameters, Risk Management & Technical Indicators Guide

> **Version:** 1.0 | **Date:** 19 March 2026 | **Scope:** All 40 stocks from the Iran War Investment Research Report
> **Purpose:** To be used as the technical reference for building the advanced trading analysis HTML page

---

## Table of Contents

1. [Overview & Philosophy](#1-overview--philosophy)
2. [Position Sizing & Capital Risk Rules](#2-position-sizing--capital-risk-rules)
3. [Stop Loss Framework](#3-stop-loss-framework)
4. [Take Profit Framework](#4-take-profit-framework)
5. [Risk/Reward Ratios](#5-riskreward-ratios)
6. [SHORT Positions — Full Trading Parameters](#6-short-positions--full-trading-parameters)
7. [BUY Positions — Full Trading Parameters](#7-buy-positions--full-trading-parameters)
8. [Technical Indicators to Display](#8-technical-indicators-to-display)
9. [Charts & Graphs to Build](#9-charts--graphs-to-build)
10. [Entry Signal Checklist](#10-entry-signal-checklist)
11. [Exit Signal Checklist](#11-exit-signal-checklist)
12. [Geopolitical Event Triggers](#12-geopolitical-event-triggers)
13. [HTML Page Architecture](#13-html-page-architecture)
14. [Data Sources for Live Charts](#14-data-sources-for-live-charts)
15. [Disclaimer](#15-disclaimer)

---

## 1. Overview & Philosophy

### Why Technical Analysis Matters on Top of Fundamental Research

The Iran War Investment Research Report gives you the **why** — the fundamental thesis for each of the 40 stocks. This trading analysis layer gives you the **when, where, and how much** — the execution parameters that determine whether a fundamentally correct thesis translates into a profitable trade.

Three principles govern all parameters in this document:

**Principle 1 — Risk first, profit second.**
Never enter a position without a predetermined stop loss. The stop loss is not optional. In war-driven markets, gaps and overnight moves can be extreme. A position without a stop loss is not a trade — it is a gamble.

**Principle 2 — Risk/reward must be at least 1:2.**
For every $1 of risk (distance from entry to stop loss), you must have at least $2 of potential profit (distance from entry to take profit). This means you can be wrong more than half the time and still be profitable over a series of trades. In this portfolio, most setups target a 1:3 ratio given the strong directional conviction.

**Principle 3 — Size positions based on risk, not conviction.**
The stronger your conviction, the more tempting it is to over-size a position. Resist this. Position size is always calculated from your maximum tolerable loss per trade (1–2% of total capital), not from your confidence level. Confidence manages entries. Risk management manages survival.

---

## 2. Position Sizing & Capital Risk Rules

### The Core Formula

This is the single most important formula in trading. Apply it to every position before entering:

```
Number of shares = (Capital × Risk%) ÷ (Entry Price − Stop Loss Price)
Position Value   = Number of shares × Entry Price
```

### Example Calculation

```
Capital:           $100,000
Risk per trade:    1% = $1,000
Stock:             AAL (American Airlines) — Short
Entry price:       $10.55
Stop loss:         $11.37 (resistance level)
Risk per share:    $11.37 − $10.55 = $0.82

Number of shares:  $1,000 ÷ $0.82 = 1,219 shares
Position value:    1,219 × $10.55 = $12,861 (12.9% of capital)
```

### Risk Per Trade — Guidelines by Account Size

| Account Size | Max Risk Per Trade | Rationale |
|-------------|-------------------|-----------|
| Under $25,000 | 1.0% | Small accounts cannot absorb multiple losses |
| $25,000–$100,000 | 1.0–1.5% | Standard professional range |
| $100,000–$500,000 | 1.0–2.0% | Larger base absorbs variance |
| Over $500,000 | 0.5–1.0% | Larger positions move markets; tighter sizing |

### Portfolio-Level Rules

- **Maximum total short exposure:** 40% of portfolio at any one time
- **Maximum total long exposure:** 60% of portfolio at any one time
- **Maximum exposure per sector:** 15% of total portfolio
- **Maximum exposure per single stock:** 5% of total portfolio
- **Correlated positions:** Airlines (AAL, ALK, Ryanair, Air France) are highly correlated — treat as one sector bucket
- **Drawdown rule:** If total portfolio is down 10% from peak, reduce all position sizes by 50% until recovery

---

## 3. Stop Loss Framework

### Three Stop Loss Methods — Use the One That Gives the Tightest Level

#### Method A — Technical Level Stop (preferred)
Place the stop just beyond the nearest key technical level:
- **Short positions:** Stop goes ABOVE the nearest resistance level (price must break up through resistance to invalidate the short)
- **Long positions:** Stop goes BELOW the nearest support level (price must break below support to invalidate the long)

#### Method B — ATR-Based Stop (for volatile war-time conditions)
ATR (Average True Range) measures how much a stock moves on average per day. In high-volatility geopolitical environments, ATR-based stops prevent being stopped out by normal daily noise.

```
Short stop loss = Entry price + (ATR × 1.5)
Long stop loss  = Entry price − (ATR × 1.5)
```

Use ATR period 14 (standard). The 1.5× multiplier is appropriate for war-time volatility. In normal markets, 1.0× is sufficient.

#### Method C — Percentage-Based Stop (baseline minimum)
For stocks where technical levels are unclear or ATR is very high:

| Stock Type | Short Stop | Long Stop |
|-----------|-----------|----------|
| High volatility (airlines, cruise) | +8–10% above entry | −8–10% below entry |
| Medium volatility (logistics, food) | +6–8% above entry | −6–8% below entry |
| Low volatility (energy majors, gold miners) | +5–7% above entry | −5–7% below entry |
| Defence primes | +7–9% above entry | −5–7% below entry |

### Stop Loss Rules — Critical Discipline Points

1. **Set the stop before you enter.** Not after. Not "when I see how it moves."
2. **Never widen a stop on a losing position.** This is the most common trading mistake. If price reaches your stop, it means your thesis was wrong — exit.
3. **Move stops to break-even once position is +1R profitable.** (1R = your initial risk distance.) This creates a free trade where worst case is scratch.
4. **Use guaranteed stops for short positions** where available through your broker. War-time gap risk is real — a ceasefire announced overnight can gap a short position 15%+ against you instantly.
5. **Short squeeze risk:** Monitor short interest ratios. Any stock with >20% short interest is a short squeeze candidate. Use tighter stops on these names.

---

## 4. Take Profit Framework

### Three Take Profit Methods

#### Method A — Technical Level Take Profit (preferred)
- **Short positions:** Take profit at the next major support level below entry
- **Long positions:** Take profit at the next major resistance level above entry

#### Method B — Risk Multiple Take Profit
```
TP1 (partial exit 50%) = Entry ± (Risk × 2)   → 1:2 risk/reward
TP2 (partial exit 30%) = Entry ± (Risk × 3)   → 1:3 risk/reward
TP3 (trail remainder)  = Trail stop, let it run
```

#### Method C — Fundamental Target Take Profit
Use analyst price targets as take profit anchors. For example:
- AAL analyst downgrade target: $8.00 → this becomes TP2
- XOM Wells Fargo target: $183 → this becomes TP2

### Scaling Out — The Professional Approach

Do not exit 100% of a position at once. Scale out in thirds:

```
Entry: 100% of planned position

TP1 (Exit 33–50%): At first resistance/support — lock in initial profit
    → Move stop to break-even on remaining position

TP2 (Exit 33%): At second resistance/support
    → Move stop to TP1 level on remaining position

TP3 (Trail remaining 17–33%): Use trailing stop of 1×ATR
    → Let war-driven momentum carry the position as far as it goes
```

This approach means:
- You always lock in some profit
- You are never stopped out of a full position at a loss once TP1 is hit
- You capture the full move if the thesis plays out

---

## 5. Risk/Reward Ratios

### Target Ratios by Position Type

| Position Category | Minimum R:R | Target R:R | Notes |
|------------------|------------|-----------|-------|
| High-conviction shorts (AAL, CCL) | 1:2 | 1:3 | Strong technical + fundamental alignment |
| Medium-conviction shorts (ULVR, NESN) | 1:2 | 1:2.5 | Less directional clarity |
| High-conviction longs (XOM, CVX, LMT, RTX) | 1:2 | 1:3–4 | Multi-month trend with strong catalysts |
| Gold miners (NEM, AEM, WPM) | 1:2 | 1:3 | Gold ATH provides strong momentum |
| Renewable energy (NEE, ENPH) | 1:1.5 | 1:2 | Longer-horizon, more mean-reversion risk |
| Defence tech (PLTR, CRWD) | 1:2 | 1:2.5 | High beta, wider price swings |

### Understanding the R Multiple System

| Scenario | Outcome |
|---------|---------|
| Hit stop loss | −1R (lose your planned risk amount) |
| Exit at TP1 | +2R |
| Exit at TP2 | +3R |
| Trail to maximum | +4R to +6R |
| Stopped at break-even | 0R (no loss, no gain) |

If you achieve an average of +2R per winning trade and lose −1R per losing trade, you are profitable even if you are only right 40% of the time.

---

## 6. SHORT Positions — Full Trading Parameters

### Section A: Airlines

#### AAL — American Airlines Group
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | $10.50–$11.00 (current range) |
| Stop loss | $11.37 (resistance) / $11.50 (ATR-based) |
| TP1 (50% exit) | $9.00 (−15% from entry) |
| TP2 (30% exit) | $8.00 (analyst downgrade target) |
| TP3 (trail 20%) | $6.50–$7.00 (pre-pandemic low analog) |
| Risk per share | ~$0.82–$1.00 |
| Reward at TP2 | ~$2.55 |
| R:R ratio | 1:2.5 to 1:3.1 |
| Max position hold | 4–6 months |
| Key risk to thesis | Sudden oil price collapse below $75/barrel |
| Short squeeze risk | MODERATE — monitor short interest weekly |
| Technical signal | MACD bearish, sell signal from pivot top Feb 26; down 24.32% |
| Fundamental catalyst | Q1 2026 earnings Apr 23 — expect miss |

#### ALK — Alaska Air Group
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current price / any bounce to 50-day MA |
| Stop loss | +9% above entry (worst performer, likely continued momentum) |
| TP1 | −15% from entry |
| TP2 | −25% from entry |
| TP3 | Trail with 1.5×ATR stop |
| R:R ratio | 1:2.8 |
| Key risk | Same as AAL — oil retreat |
| Note | Down 23.8% since conflict — momentum strongly bearish |

#### RYA.L — Ryanair
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Any bounce toward 20-day MA |
| Stop loss | Above 50-day MA (approx +7–8% from entry) |
| TP1 | Previous support −12% |
| TP2 | −20–22% (52-week low territory) |
| R:R ratio | 1:2.5 |
| Currency note | GBP-denominated — hedge GBP/USD if USD-based portfolio |

#### AF.PA — Air France-KLM
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current levels / bounce to resistance |
| Stop loss | +8% above entry |
| TP1 | −15% |
| TP2 | −25% |
| R:R ratio | 1:3 |
| Currency note | EUR-denominated |

---

### Section B: Cruise Lines & Hotels

#### CCL — Carnival Corp
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | $24.50–$25.50 (current trading range) |
| Stop loss | $27.50 (+8–10% above entry — above recent resistance) |
| TP1 (50% exit) | $21.00 (−12–14% from entry) |
| TP2 (30% exit) | $18.00 (−24–25%) |
| TP3 (trail 20%) | $14.00–$16.00 (deep fundamental bear case) |
| Risk per share | ~$2.50–$3.00 |
| Reward at TP2 | ~$6.00–$7.00 |
| R:R ratio | 1:2.3 to 1:2.8 |
| Key risk | Fuel hedging announcement / oil price drop |
| Fundamental trigger | Marine gasoil $700→$1,500 per ton — no hedge |
| Technical watch | RSI approaching oversold — tighten TP1 if RSI <35 |

#### NCLH — Norwegian Cruise Line
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce to 20-day MA |
| Stop loss | +9% above entry |
| TP1 | −12% |
| TP2 | −22% |
| R:R ratio | 1:2.4 |

#### AC.PA — Accor SA
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Any bounce to prior breakdown level |
| Stop loss | +8% above entry |
| TP1 | −12% |
| TP2 | −20% |
| R:R ratio | 1:2.5 |
| Currency note | EUR-denominated |

#### IHG — InterContinental Hotels
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce toward 50-day MA |
| Stop loss | +7% above entry |
| TP1 | −10% |
| TP2 | −18% |
| R:R ratio | 1:2.6 |
| Conviction | Medium — less aggressive than CCL/NCLH |

---

### Section C: Logistics & Shipping

#### FDX — FedEx
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / any bounce |
| Stop loss | +7% above entry |
| TP1 | −12% |
| TP2 | −20% |
| R:R ratio | 1:2.9 |
| Note | Monitor fuel surcharge announcements — may partially offset |

#### UPS — United Parcel Service
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current levels |
| Stop loss | +7% above entry |
| TP1 | −10% |
| TP2 | −18% |
| R:R ratio | 1:2.6 |

#### ZIM — ZIM Integrated Shipping
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce |
| Stop loss | +10% above entry (high volatility stock) |
| TP1 | −20% |
| TP2 | −35% |
| R:R ratio | 1:3.5 |
| Risk note | Very high volatility — reduce position size by 30% vs standard |

#### DPSGY — DHL Group
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce to resistance |
| Stop loss | +7% above entry |
| TP1 | −10% |
| TP2 | −16% |
| R:R ratio | 1:2.3 |
| Conviction | Medium — lower direct exposure vs FDX/UPS |

---

### Section D: Technology (Asia-Exposed)

#### 9984.T — SoftBank Group
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Any bounce / current |
| Stop loss | +9% above entry |
| TP1 | −15% |
| TP2 | −25% |
| R:R ratio | 1:2.8 |
| Currency note | JPY-denominated — monitor USD/JPY |

#### SMSN.L — Samsung GDR
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current levels |
| Stop loss | +8% above entry |
| TP1 | −14% |
| TP2 | −22% |
| R:R ratio | 1:2.75 |

#### INFY — Infosys ADR
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Bounce toward 50-day MA |
| Stop loss | +7% above entry |
| TP1 | −10% |
| TP2 | −17% |
| R:R ratio | 1:2.4 |
| Conviction | Medium |

#### 005930.KS — SK Hynix
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce |
| Stop loss | +9% above entry |
| TP1 | −15% |
| TP2 | −24% |
| R:R ratio | 1:2.7 |

---

### Section E: Insurance

#### MUV2.DE — Munich Re
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce to resistance |
| Stop loss | +6% above entry (lower volatility stock) |
| TP1 | −10% |
| TP2 | −17% |
| R:R ratio | 1:2.8 |

#### SREN.SW — Swiss Re
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce |
| Stop loss | +6% above entry |
| TP1 | −9% |
| TP2 | −15% |
| R:R ratio | 1:2.5 |
| Conviction | Medium |

---

### Section F: Food & Agriculture

#### ADM — Archer-Daniels-Midland
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Current / bounce to 20-day MA |
| Stop loss | +7% above entry |
| TP1 | −12% |
| TP2 | −20% |
| R:R ratio | 1:2.9 |

#### ULVR.L — Unilever
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Any rally to prior support-turned-resistance |
| Stop loss | +6% above entry |
| TP1 | −9% |
| TP2 | −15% |
| R:R ratio | 1:2.5 |
| Conviction | Medium |

#### NESN.SW — Nestlé
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Any bounce |
| Stop loss | +6% above entry |
| TP1 | −9% |
| TP2 | −14% |
| R:R ratio | 1:2.3 |
| Conviction | Medium |

#### 9983.T — Fast Retailing
| Parameter | Value |
|-----------|-------|
| Direction | SHORT |
| Entry zone | Bounce toward 50-day MA |
| Stop loss | +8% above entry |
| TP1 | −12% |
| TP2 | −20% |
| R:R ratio | 1:2.5 |

---

## 7. BUY Positions — Full Trading Parameters

### Section A: US Energy Majors & MLPs

#### XOM — ExxonMobil
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current price / any pullback to 20-day MA |
| Stop loss | −6% below entry (below recent swing low) |
| TP1 (33% exit) | +12% from entry |
| TP2 (33% exit) | +20% (Wells Fargo target $183) |
| TP3 (trail 33%) | Trail with 2×ATR stop — let war premium run |
| R:R ratio | 1:3.3 |
| Dividend yield | 3.4% — adds to total return while holding |
| Max hold | 12 months |
| Key risk | Oil price collapse below $75/barrel on ceasefire |
| Breakeven oil | ~$35/barrel — massive safety margin at $104 |

#### CVX — Chevron
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / any 3–5% pullback |
| Stop loss | −6% below entry |
| TP1 | +10% |
| TP2 | +18% |
| TP3 | Trail 2×ATR |
| R:R ratio | 1:3.0 |
| Dividend yield | 4.1% |

#### EPD — Enterprise Products Partners
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current levels — MLP distributions paid quarterly |
| Stop loss | −5% below entry (low volatility, pipeline MLP) |
| TP1 | +10% (capital gain component) |
| TP2 | +18% |
| Total return target | +24% (capital + 5.9% dividend yield × 12 months) |
| R:R ratio | 1:3.6 (including yield) |
| Key advantage | Earns on volume not price — resilient to oil pullbacks |

#### MPLX — MPLX LP
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current |
| Stop loss | −5% below entry |
| TP1 | +10% |
| TP2 | +17% |
| Total return | +24–25% (capital + 7.4% yield) |
| R:R ratio | 1:3.4 including yield |

---

### Section B: Defence & Aerospace

#### LMT — Lockheed Martin
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / pullback to 20-day MA |
| Stop loss | −7% below entry |
| TP1 (33% exit) | +12% |
| TP2 (33% exit) | +20% |
| TP3 (trail 33%) | Trail 1.5×ATR — defence contracts are multi-year |
| R:R ratio | 1:2.9 |
| Catalyst | NATO procurement wave + Gulf state orders post-war |
| Hold period | 6–12 months minimum |

#### RTX — RTX Corp
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Any pullback from record $215 high |
| Stop loss | −7% below entry |
| TP1 | +10% |
| TP2 | +18% |
| TP3 | Trail — $215 record may break through $240+ |
| R:R ratio | 1:2.6 |
| Note | $115M Alabama expansion confirms capacity lock-in |

#### NOC — Northrop Grumman
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / 3–5% pullback |
| Stop loss | −7% below entry |
| TP1 | +12% |
| TP2 | +20% |
| R:R ratio | 1:2.9 |

#### DRS — Leonardo DRS
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current — mid-cap, more room to run |
| Stop loss | −9% below entry (higher volatility mid-cap) |
| TP1 | +15% |
| TP2 | +28% |
| R:R ratio | 1:3.0 |
| Position sizing | Reduce to 60–70% of standard size (smaller cap) |

---

### Section C: Gold & Precious Metals

#### NEM — Newmont Corp
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / any pullback to 20-day MA |
| Stop loss | −7% below entry |
| TP1 (33% exit) | +15% |
| TP2 (33% exit) | +25% |
| TP3 (trail 33%) | Trail 2×ATR — gold at ATH has room to extend |
| R:R ratio | 1:3.6 |
| Leverage effect | Miners move 2–3× gold — at $5,014 gold, NEM is printing cash |
| Key risk | Gold price reversal on ceasefire / Fed hawkishness |

#### AEM — Agnico Eagle
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / pullback to support |
| Stop loss | −7% below entry |
| TP1 | +14% |
| TP2 | +23% |
| R:R ratio | 1:3.3 |
| Advantage | Stable Canadian/Finnish jurisdiction — no operational geo-risk |

#### WPM — Wheaton Precious Metals
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current |
| Stop loss | −6% below entry |
| TP1 | +12% |
| TP2 | +20% |
| R:R ratio | 1:3.3 |
| Advantage | Streaming model — no cost inflation risk, pure price exposure |

---

### Section D: Defence Technology & Cybersecurity

#### PLTR — Palantir Technologies
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / pullback to 20-day MA |
| Stop loss | −10% below entry (higher beta tech stock) |
| TP1 (33% exit) | +15% |
| TP2 (33% exit) | +25% |
| TP3 (trail 33%) | Trail 2×ATR |
| R:R ratio | 1:2.5 |
| Beta note | PLTR moves more violently than energy/defence — adjust position size |

#### CRWD — CrowdStrike
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Any pullback / current |
| Stop loss | −10% below entry |
| TP1 | +15% |
| TP2 | +25% |
| R:R ratio | 1:2.5 |
| Catalyst | Iran cyberattacks = recurring demand driver |

#### AXON — Axon Enterprise
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / pullback |
| Stop loss | −9% |
| TP1 | +14% |
| TP2 | +22% |
| R:R ratio | 1:2.4 |

#### HII — Huntington Ingalls
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / 3–5% pullback |
| Stop loss | −7% |
| TP1 | +12% |
| TP2 | +20% |
| R:R ratio | 1:2.9 |
| Note | Sole-source nuclear carrier — no earnings surprise risk to downside |

---

### Section E: Renewables, Fertilizer & Domestic Food

#### NEE — NextEra Energy
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / any rate-fear dip |
| Stop loss | −7% below entry |
| TP1 | +10% |
| TP2 | +18% |
| R:R ratio | 1:2.6 |
| Timeline | Best 6–12 month hold — rate narrative takes time to shift |

#### CF — CF Industries
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current — planting season window is NOW |
| Stop loss | −7% below entry |
| TP1 (50% exit) | +15% (US urea pricing power near-term) |
| TP2 (30% exit) | +25% |
| TP3 (trail 20%) | Trail 1.5×ATR |
| R:R ratio | 1:3.6 |
| Urgency | Planting season Mar–Jun = maximum pricing power window |

#### MOS — Mosaic Company
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current |
| Stop loss | −7% |
| TP1 | +15% |
| TP2 | +25% |
| R:R ratio | 1:3.6 |

#### TSN — Tyson Foods
| Parameter | Value |
|-----------|-------|
| Direction | LONG |
| Entry zone | Current / minor pullback |
| Stop loss | −6% |
| TP1 | +10% |
| TP2 | +16% |
| R:R ratio | 1:2.7 |
| Conviction | Medium |

---

## 8. Technical Indicators to Display

These are the indicators that should appear on the advanced trading analysis HTML page for each stock. All can be embedded via TradingView widgets or documented as static analysis.

### Tier 1 — Core Indicators (Display for ALL 40 stocks)

#### RSI — Relative Strength Index
- **Period:** 14 (standard)
- **Overbought zone:** Above 70 → Bearish signal (confirms short entries, warns longs to take partial profit)
- **Oversold zone:** Below 30 → Bullish signal (warns shorts to cover, confirms long entries)
- **How to display:** Gauge/dial widget + current reading + trend direction (rising/falling)
- **War-time note:** In strong trending markets (like this war-driven move), RSI can stay overbought or oversold for extended periods. Do not use RSI alone — always confirm with MACD.
- **Current AAL reading:** RSI bearish — sell signal confirmed on all moving averages

#### MACD — Moving Average Convergence Divergence
- **Settings:** Fast EMA 12, Slow EMA 26, Signal line 9 (standard settings)
- **Buy signal:** MACD line crosses ABOVE signal line (histogram turns positive/green)
- **Sell signal:** MACD line crosses BELOW signal line (histogram turns negative/red)
- **How to display:** Mini histogram chart per stock + current cross direction
- **War-time use:** MACD is a trend-following indicator — ideal for war-driven directional moves. Use MACD to confirm entry direction; use RSI to time the exact entry.
- **Combining RSI + MACD:** Pairing RSI with MACD has produced a 77% win rate in backtesting (Gate.io, Jan 2026)

#### Bollinger Bands
- **Settings:** 20-period SMA, 2 standard deviations (standard)
- **Upper band touch:** Overbought — confirms short entries, warns longs
- **Lower band touch:** Oversold — confirms long entries, warns shorts
- **Band squeeze:** Narrowing bands = imminent breakout (directional confirmation needed from RSI/MACD)
- **Band expansion:** Widening bands = strong trend in progress — stay with the trend
- **How to display:** Show current band position (upper/middle/lower) as a position indicator per stock

### Tier 2 — Supplementary Indicators (Display for high-conviction positions)

#### ATR — Average True Range
- **Period:** 14
- **Use:** Calculating stop loss distances (Entry ± 1.5×ATR)
- **War-time note:** ATR will be elevated during conflict — this means wider stops are needed, which means smaller position sizes
- **How to display:** Current ATR value + recommended stop distance in $ and %

#### Moving Averages
- **20-day EMA:** Short-term trend direction
- **50-day MA:** Medium-term support/resistance
- **200-day MA:** Long-term trend (above = bullish, below = bearish)
- **Death Cross:** 50-day crosses below 200-day = strong bearish signal (confirms shorts)
- **Golden Cross:** 50-day crosses above 200-day = strong bullish signal (confirms longs)
- **Current AAL:** Short and long-term MAs both giving sell signals. Long-term average above short-term = confirmed downtrend.
- **How to display:** Traffic light system — Green (price above 200MA), Amber (between 50 and 200MA), Red (below both MAs)

#### Volume Analysis
- **Volume spike on price drop:** Bearish confirmation for shorts
- **Volume spike on price rise:** Bullish confirmation for longs
- **Volume decrease on price move:** Weak move — potential reversal
- **AAL note:** Volume rose on falling prices — bearish confirmation signal
- **How to display:** Volume bar chart with average volume line overlay

#### Fibonacci Retracement Levels
- **Key levels:** 23.6%, 38.2%, 50%, 61.8%, 78.6%
- **Use for shorts:** Short entry on bounce to 38.2% or 50% retracement after breakdown
- **Use for longs:** Long entry on pullback to 38.2% or 50% retracement after breakout
- **How to display:** Show Fibonacci level where current price sits relative to recent swing high/low

### Tier 3 — Advanced Indicators (Optional, for sophisticated analysis page)

#### Stochastic Oscillator
- **Settings:** 14, 3, 3
- **Use:** Confirming RSI signals in ranging markets
- **Overbought:** Above 80 | **Oversold:** Below 20
- **Best use:** Pair with MACD to filter false signals in sideways-trending stocks

#### On-Balance Volume (OBV)
- **Use:** Confirms whether volume is flowing into or out of a stock
- **Divergence signal:** Price rises but OBV falls = distribution (smart money selling) → confirms short
- **Convergence signal:** Price falls but OBV rises = accumulation → confirms long entry

#### Short Interest Ratio
- **Definition:** Number of shares sold short ÷ average daily volume
- **High risk threshold:** Short interest ratio >5 days → short squeeze risk elevated
- **Very high risk:** >10 days → dangerous for short sellers
- **Display:** Show as a number + warning flag if above threshold

---

## 9. Charts & Graphs to Build

These are the specific visual elements to include on the advanced trading analysis HTML page.

### Chart 1 — Position Overview Dashboard
**Type:** Horizontal bar chart (Chart.js)
**Data:** Risk% and Reward% for all 40 stocks side by side
**Colours:** Red bars for shorts, green bars for longs
**X-axis:** Percentage move (−40% to +40%)
**Shows:** Stop loss distance and TP1/TP2 targets visually

### Chart 2 — Risk/Reward Matrix
**Type:** Scatter plot (Chart.js)
**X-axis:** Risk % (stop loss distance)
**Y-axis:** Reward % (TP2 target)
**Bubble size:** Position conviction (High/Medium)
**Colours:** Red bubbles = shorts, Green bubbles = longs
**Insight:** Instantly shows which trades have the best risk-adjusted setups

### Chart 3 — Technical Signal Heat Map
**Type:** Grid/table with colour-coded cells (HTML/CSS)
**Rows:** All 40 stocks
**Columns:** RSI status | MACD signal | Bollinger Band position | MA trend | Overall signal
**Colours:** Green = bullish, Red = bearish, Amber = neutral
**Purpose:** One-glance view of technical alignment across the full portfolio

### Chart 4 — Portfolio Risk Exposure Pie Chart
**Type:** Doughnut chart (Chart.js)
**Segments:** By sector — Airlines, Cruise/Hotels, Logistics, Tech, Insurance, Food (shorts) + Energy, Defence, Gold, Cyber, Fertilizer, Renewables (longs)
**Shows:** How much of total risk budget is allocated to each sector

### Chart 5 — Stop Loss & Take Profit Level Table
**Type:** Structured HTML table with colour coding
**Columns:** Ticker | Direction | Entry | Stop Loss | TP1 | TP2 | TP3 | R:R Ratio
**Colour coding:** Short rows = red border, Long rows = green border
**Feature:** Sortable by R:R ratio, sector, conviction level

### Chart 6 — Macro Correlation Tracker
**Type:** Line chart (Chart.js)
**Lines:** Brent crude price | Gold price | VIX | Average of short basket | Average of long basket
**X-axis:** Date (rolling 90-day window)
**Purpose:** Shows how portfolio positions correlate with macro war drivers
**Update frequency:** Weekly (manual update of data array in JS)

### Chart 7 — Trade Journal / P&L Tracker
**Type:** Interactive table + running P&L line chart
**Input fields:** Entry date | Ticker | Direction | Entry price | Current price | Stop | TP
**Auto-calculates:** Open P&L in $ and % | R multiple achieved | Days held
**Running total:** Portfolio P&L chart updates as positions are entered

### Chart 8 — RSI Gauge Widgets
**Type:** Semi-circular gauge (SVG/CSS)
**One gauge per stock** (or top 10 highest conviction positions)
**Shows:** Current RSI reading with overbought/oversold zones highlighted
**Purpose:** Visual RSI dashboard — instantly see which positions are at extremes

---

## 10. Entry Signal Checklist

Before entering any position, verify at least 3 of these 5 conditions are met:

### For SHORT entries:
- [ ] **Fundamental:** Gulf exposure / fuel cost / supply chain thesis confirmed and current
- [ ] **RSI:** Above 60 (approaching overbought on bounce) OR below 50 and falling
- [ ] **MACD:** Bearish crossover confirmed OR histogram turning from positive to negative
- [ ] **Moving Average:** Price below 50-day MA OR 50-day crossing below 200-day (Death Cross)
- [ ] **Bollinger Bands:** Price touching or near upper band on low-conviction bounce

### For LONG entries:
- [ ] **Fundamental:** Oil price, defence contract, gold, or fertilizer thesis active and strengthening
- [ ] **RSI:** Below 40 on pullback entry (oversold on dip) OR above 50 and rising (momentum)
- [ ] **MACD:** Bullish crossover OR histogram turning positive
- [ ] **Moving Average:** Price above 50-day MA OR Golden Cross recently confirmed
- [ ] **Bollinger Bands:** Price holding above middle band OR bouncing from lower band

### Entry timing principle:
Do NOT enter immediately on a large gap move. War news creates gaps that partially fill. Wait for the first pullback or consolidation before entering. For shorts — enter on bounces, not on breakdown days. For longs — enter on dips, not on breakout days.

---

## 11. Exit Signal Checklist

### Exit a SHORT position when:
- [ ] Stop loss hit (mandatory exit — no exceptions)
- [ ] RSI drops below 30 (stock oversold — cover at least 50% of position)
- [ ] MACD bullish crossover confirmed
- [ ] Brent crude drops below $80/barrel (fundamental thesis weakens)
- [ ] Ceasefire announced or Hormuz reopening confirmed (immediate exit)
- [ ] Short interest ratio exceeds 15 days (short squeeze risk critical)
- [ ] TP1 or TP2 hit (scale out per plan)

### Exit a LONG position when:
- [ ] Stop loss hit (mandatory exit — no exceptions)
- [ ] RSI rises above 75 (take partial profit, tighten trailing stop)
- [ ] MACD bearish crossover confirmed
- [ ] Gold breaks below $4,500 (for gold miner longs)
- [ ] Oil drops below $80 (for energy longs — re-assess)
- [ ] Ceasefire + Hormuz reopening (partially exit energy/defence longs, hold gold)
- [ ] TP1 or TP2 hit (scale out per plan)

---

## 12. Geopolitical Event Triggers

These are the specific geopolitical events that require immediate portfolio review and potential position changes.

| Event | Impact | Action Required |
|-------|--------|----------------|
| Ceasefire announced | Oil -20 to -30%, Gold -10%, Airlines +15–20% | Immediately cover airline/cruise shorts; reduce energy longs 50%; hold gold longs; hold defence |
| Hormuz fully reopened | Same as ceasefire | Same as above |
| Iran nuclear facility struck | Oil +10–15%, Gold +5%, Defence +5–8% | Add to defence longs; hold energy; tighten airline short stops |
| US carrier group deployed | Markets stabilise, VIX drops | Defence longs strengthen; neutral on rest |
| Israeli ground escalation | Oil +10–20%, VIX spikes | All shorts strengthen; all energy/gold longs strengthen |
| Gulf state peace deal | Mixed — watch oil price | Re-assess hotel/tourism shorts; hold energy |
| China intervenes diplomatically | Oil -5%, VIX -15% | Partial de-risk of shorts; trim energy longs |
| Russia enters conflict | Oil +25–40%, Global equity crash | Maximum short exposure; maximum energy/gold/defence longs |
| Iran attacks Saudi Aramco | Oil +30–50%, insurance crisis | All shorts valid; all energy longs at maximum |
| US elections change policy | Uncertain | Monitor closely; no pre-emptive action |

---

## 13. HTML Page Architecture

### Recommended Page Structure for the Advanced Trading Analysis Page

```
index_trading.html (or trading-analysis.html)
│
├── HEADER SECTION
│   ├── Page title + last updated date
│   ├── Brent crude / Gold / VIX live macro ticker strip
│   └── Portfolio summary: X shorts active | Y longs active | Total R deployed
│
├── TAB 1 — TRADING PARAMETERS
│   ├── Full table: All 40 stocks with Entry/Stop/TP1/TP2/TP3/R:R
│   ├── Filter buttons: All | Shorts | Longs | High Conviction | By Sector
│   └── Click-to-expand: Full technical analysis per stock
│
├── TAB 2 — TECHNICAL SIGNALS
│   ├── Heat map: RSI + MACD + BB + MA status for all 40 stocks
│   ├── RSI gauge widgets (top 10 positions)
│   └── Entry/exit signal checklist tracker
│
├── TAB 3 — CHARTS & VISUALISATIONS
│   ├── Chart 1: Stop loss vs Take profit bar chart
│   ├── Chart 2: Risk/Reward scatter matrix
│   ├── Chart 3: Portfolio sector allocation doughnut
│   └── Chart 4: Macro correlation tracker
│
├── TAB 4 — RISK MANAGEMENT
│   ├── Position sizing calculator (interactive inputs)
│   ├── Portfolio exposure meters (by sector, by direction)
│   ├── Drawdown tracker
│   └── Correlation risk warnings
│
├── TAB 5 — TRADE JOURNAL
│   ├── Add/edit trade form
│   ├── Open positions table with live P&L
│   ├── Closed trades history
│   └── Running P&L line chart
│
├── TAB 6 — GEOPOLITICAL TRIGGERS
│   ├── Event trigger table
│   ├── Scenario analysis (ceasefire, escalation, etc.)
│   └── Position adjustment guide per scenario
│
└── FOOTER
    ├── Link back to main research report
    ├── Last updated timestamp
    └── Disclaimer
```

### Recommended Tech Stack for the New Page

| Element | Technology | Reason |
|---------|-----------|--------|
| Charts | Chart.js 4.4.1 | Already used in main report |
| RSI Gauges | SVG + CSS animation | Lightweight, no dependencies |
| Heat map | Pure HTML/CSS grid | Fast rendering |
| Position calculator | Vanilla JS | No framework needed |
| Trade journal storage | localStorage (browser) | Persists between sessions without a backend |
| TradingView widgets | TradingView embed | Free live charts for any ticker |
| Styling | Same CSS variables as main report | Consistent design system |

### TradingView Chart Embed Code Template

To embed a live TradingView chart for any stock, use:

```html
<div class="tradingview-widget-container">
  <div id="tradingview_TICKER"></div>
  <script type="text/javascript" src="https://s3.tradingview.com/tv.js"></script>
  <script type="text/javascript">
    new TradingView.widget({
      "width": "100%",
      "height": 400,
      "symbol": "NASDAQ:AAL",
      "interval": "D",
      "timezone": "Etc/UTC",
      "theme": "light",
      "style": "1",
      "locale": "en",
      "toolbar_bg": "#f1f3f6",
      "enable_publishing": false,
      "studies": [
        "RSI@tv-basicstudies",
        "MACD@tv-basicstudies",
        "BB@tv-basicstudies"
      ],
      "container_id": "tradingview_TICKER"
    });
  </script>
</div>
```

Replace `"NASDAQ:AAL"` with the correct exchange:ticker for each stock.

---

## 14. Data Sources for Live Charts

| Data Type | Free Source | Update Frequency |
|-----------|------------|-----------------|
| Stock prices | Yahoo Finance API (unofficial) | Real-time (15min delay free) |
| Stock prices | Alpha Vantage API (free tier) | Daily |
| Brent crude | EIA API (US Energy Info Admin) | Daily |
| Gold price | Metals API (free tier) | Daily |
| VIX | CBOE (via Yahoo Finance) | Real-time |
| Economic calendar | Investing.com embed | Daily |
| TradingView charts | TradingView widgets (free) | Real-time |
| News feed | Reuters RSS / Google News RSS | Hourly |

> Note: For a static GitHub Pages site, the easiest approach is manually updating a JavaScript data object weekly rather than building API integrations. Full API integration requires either a backend server or a third-party data service.

---

## 15. Disclaimer

> This trading analysis documentation is for **educational and informational purposes only**. All stop loss levels, take profit targets, position sizing formulas, and technical analysis parameters described in this document are illustrative examples based on commonly used trading methodologies. They do not constitute financial advice, investment recommendations, or a solicitation to buy or sell any security.
>
> Trading and short selling involve significant risk of loss, including the possible loss of all capital invested. Short selling carries theoretically unlimited loss potential. Past performance of any indicator or strategy does not guarantee future results. Technical analysis signals can and do fail. Geopolitical events are inherently unpredictable and can cause sudden, extreme price movements that invalidate any pre-planned parameters.
>
> Always consult a qualified, licensed financial advisor before implementing any trading strategy. Ensure you fully understand margin requirements, borrowing costs for short selling, and the tax implications of short-term trading in your jurisdiction before executing any trades.

---

*Document version: 1.0 | Created: 19 March 2026 | Repository: benimanfouo/Iran_War_Investment_Research_Report_2026*
