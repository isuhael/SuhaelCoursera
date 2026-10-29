# Zerodha transaction costs and the arithmetic of ₹2,000/day (and 5–7%/month) on ₹1,00,000 capital

As of 2026-10-29. **How these numbers were sourced:** zerodha.com and icicidirect.com could not be reached from this research session (DNS blocked). All Zerodha figures below come from search-engine extracts of zerodha.com/charges, support.zerodha.com and kite.trade pages, plus third-party pages, not from a direct page load. The two cached versions of zerodha.com/charges disagree slightly (see Q1). **Before using any number for live trading, re-check it on zerodha.com/charges and the Zerodha brokerage calculator.** Every calculation is shown so it can be re-run with corrected inputs. Where a figure comes from my background knowledge rather than a source found in this session, it is labelled that way.

---

## Q1. Current Zerodha charge schedule by segment (and Budget changes)

### Takeaway
The pricing model is unchanged: ₹0 brokerage on delivery, and ₹20 per order (or 0.03% if lower) on everything else. The cost that changed is statutory. **Union Budget 2026-27 raised STT on futures from 0.02% to 0.05% and on options from 0.10% to 0.15% of premium (exercise: 0.125% to 0.15%), effective 1 April 2026.** This came on top of the October 2024 hike. For a Nifty futures round trip, STT is now about 84% of total cost.

### Cited Findings

**Brokerage (Zerodha)**
- Equity delivery ₹0. Equity intraday and futures: ₹20 or 0.03% per executed order, whichever is lower. Options: flat ₹20 per executed order — [Zerodha charges page (via search extract)](https://zerodha.com/charges/); [Chittorgarh Zerodha brokerage 2026](https://www.chittorgarh.com/brokerage_charges/zerodha/18/)

**STT / CTT (statutory, after 1 April 2026)**
- Futures: 0.05% on the sell side (₹50 per lakh). Options sold or shorted: 0.15% of premium on the sell side. Options exercised: 0.15% of intrinsic value. Before the change: 0.02% futures, 0.1% options sold, 0.125% exercised — [Zerodha Support: STT rates and how to calculate it](https://support.zerodha.com/category/account-opening/resident-individual/ri-charges/articles/how-is-the-securities-transaction-tax-stt-calculated)
- Budget 2026-27 (presented 1 Feb 2026): futures STT 0.02% to 0.05%, options premium 0.1% to 0.15%, exercise 0.125% to 0.15%. Most sources give 1 April 2026 as the effective date, and exchange circulars dated 31 March 2026 implemented the new rates — [5paisa: STT hike on F&O from April 1](https://www.5paisa.com/news/stt-hike-on-fo-to-take-effect-from-april-1-amid-rising-options-activity); [IANS: FM hikes STT on futures to 0.05%](https://ianslive.in/fm-sitharaman-hikes-stt-on-futures-to-005-pc-in-budget-2026--20260201131104); [ICICI Direct: STT changes in Budget 2026](https://www.icicidirect.com/ilearn/futures-and-options/articles/stt-changes-in-budget-2026-what-f-o-traders-should-know); [Zerodha After-market report: STT hike triggers budget-day sell-off](https://aftermarketreport.zerodha.com/p/stt-hike-triggers-sharp-budget-day). One aggregator labels its table "New Rate (Feb 1, 2026)". That is the announcement date, not the effective date — [1Finance](https://1finance.co.in/blog/stt-futures-options-increased-budget-2026-for-fno-investors/). Market experts expected the hike to cut trading volumes by 20–30% — [Outlook Money](https://www.outlookmoney.com/invest/budget-2026-market-experts-suggest-stt-hike-likely-to-dent-trading-volumes-by-20-30)
- Equity STT was not changed: delivery 0.1% on buy and sell, intraday 0.025% on the sell side — [Zerodha Support STT article](https://support.zerodha.com/category/account-opening/resident-individual/ri-charges/articles/how-is-the-securities-transaction-tax-stt-calculated); [knowyourbrokerage Zerodha charges 2026](https://knowyourbrokerage.in/zerodha/charges)
- Commodity CTT: 0.01% on the sell side for non-agri futures (on notional value, price × lot), and 0.05% on the sell side for options — [Zerodha charges page (via search extract)](https://zerodha.com/charges?c=ZMPCDF); [Kotak: what is CTT](https://www.kotaksecurities.com/investing-guide/share-market/what-is-commodity-transaction-tax)
- Currency derivatives carry no STT. *(Background knowledge; not re-verified this session.)*

**Exchange transaction charges (as displayed by Zerodha)**

| Segment | NSE | BSE | MCX |
|---|---|---|---|
| Equity delivery and intraday | 0.00307% (older page version: 0.00297%) | 0.00375% | – |
| Equity futures | 0.00183% (older: 0.00173%) | 0 | – |
| Equity options (on premium) | 0.03553% (older: 0.03503%) | 0.0325% | – |
| Currency futures | 0.00035% | 0.00045% | – |
| Commodity futures | 0.0001% | – | 0.0021% |
| Commodity options (on premium) | 0.001% | – | 0.0418% |

  Sources: [Zerodha charges page (via search extract)](https://zerodha.com/charges/); [Zerodha Support: exchange transaction charges](https://support.zerodha.com/category/account-opening/resident-individual/ri-charges/articles/exchange-transaction-charges). Older aggregator figures (NSE equity 0.00325%, futures 0.0019%, options 0.053%) predate the October 2024 "true-to-label" revision and are out of date — [search extract of 2024-era calculators, e.g. top10stockbroker](https://top10stockbroker.com/zerodha-brokerage-charges/)
- NSE Investor Protection Fund Trust (IPFT) charge on options: ₹50 per crore of premium, plus GST — [Zerodha charges page (via search extract)](https://zerodha.com/charges?c=ZMPCDF)
- MCX levies a transaction charge on every trade it clears, and Zerodha passes it through at the exchange rate — [Zerodha Support: MCX transaction charges logic](https://support.zerodha.com/category/account-opening/charges-at-zerodha/articles/what-is-the-logic-behind-mcx-transactions-and-why-is-it-not-the-same-for-all-brokers)

**SEBI fee, stamp duty, GST, DP**
- SEBI turnover fee: ₹10 per crore (0.0001%) — [Zerodha charges page (via search extract)](https://www.zerodha.com/charges)
- Stamp duty, buy side only: options 0.003% (₹300 per crore) — [Zerodha charges page](https://www.zerodha.com/charges). Delivery 0.015%, intraday 0.003%, futures 0.002%, commodity futures 0.002%, commodity options 0.003%. *(These come from the Indian Stamp Act schedule in force since July 2020, as shown on Zerodha's page. They are background knowledge and were not individually confirmed in a search extract this session.)*
- GST: 18% on (brokerage + SEBI fee + transaction charges). There is no GST on STT or stamp duty — [Zerodha charges page](https://www.zerodha.com/charges)
- DP charge on delivery sells: ₹15.34 per scrip per day (₹3.50 CDSL + ₹9.50 Zerodha + GST), however many shares are sold. Female first holders get ₹0.25 off the CDSL fee (≈ ₹15.05) — [Zerodha pricing/charges (via search extract)](https://zerodha.com/charges); [Finology: DP charges in Zerodha](https://select.finology.in/articles/broker/dp-charges-in-zerodha)

### Inferences
- **The two Zerodha page versions are consistent once IPFT is included.** The newer figures equal the older NSE "true-to-label" rates plus the NSE IPFT charge: 0.00297% + 0.0001% (₹10/cr) = 0.00307%; 0.00173% + 0.0001% = 0.00183%; 0.03503% + 0.0005% (₹50/cr) = 0.03553%. The worked examples below use the higher, all-in figures.
- **The "STT trap" on expiring ITM options has essentially disappeared.** Exercise STT (0.15% of intrinsic) now equals sell-side STT (0.15% of premium). For a contract that is 100 points ITM at expiry, both cost 0.15% × 100 × 65 = ₹9.75. Before April 2026, exercise (0.125%) cost more than selling (0.10%).
- History of F&O STT, from my background knowledge: Union Budget July 2024 raised futures STT from 0.0125% to 0.02% and options from 0.0625% to 0.1%, effective 1 Oct 2024. The Zerodha article's "previous rates" (0.02% and 0.1%) are consistent with this. Budget 2026 raised them again. Cumulatively, futures STT is now 4x and options STT 2.4x the pre-October-2024 levels.
- Statutory costs are now the main cost of F&O, not brokerage. On a Nifty futures round trip, STT is ₹737.75 of ₹881.67 (84%). On a ₹150-premium option round trip, ₹40 brokerage plus ₹7.20 GST on it is the largest part (≈ 67%).

### Gaps
- I could not load zerodha.com/charges directly. In particular, I could not confirm whether the displayed NSE rates of 0.00307% / 0.00183% / 0.03553% are the current version or whether IPFT is billed separately.
- I found no Union Budget 2025 (Feb 2025) change to STT, exchange fees or stamp duty for these segments, and no evidence of changes after Budget 2026 (e.g., a mid-2026 SEBI fee or stamp duty revision). This is "not found", not "confirmed absent".
- I did not verify the currency options exchange rate, Zerodha's ₹50 + GST call-and-trade / auto square-off fees, or brokerage on exercised options.

---

## Q2. Lot sizes, contract values, margins and minimum capital per lot

### Takeaway
After SEBI's 2024 framework and NSE's December 2025/January 2026 revision, **one Nifty futures lot (65 × ~22,700 ≈ ₹14.75 lakh notional) needs roughly ₹1.1–1.5 lakh of margin, which is more than the entire ₹1 lakh account.** Sensex (20 units) and Bank Nifty (30 units) are sized similarly. On ₹1 lakh, the index contracts realistically open to this account are **option buying** (≈ ₹6.5k–13k premium per Nifty lot) and **small MCX contracts** (Crude Mini, Gold Petal/Guinea, Silver Micro). Gold Mini and Silver Mini each tie up 40–100% of capital.

### Cited Findings
- **Nifty 50 lot = 65** (was 75). **Bank Nifty = 30** (was 35). FinNifty 60 (was 65). Midcap Select 120 (was 140). Weekly contracts switched from the 6 Jan 2026 expiry and monthly from the 27 Jan 2026 expiry — [Sahi: Nifty lot size 2026](https://www.sahi.com/blogs/nifty-lot-size-2026-bank-nifty-sensex); [HDFC Sky: NSE revises lot sizes effective January 2026](https://hdfcsky.com/news/nse-revises-market-lot-sizes-for-major-index-derivatives-effective-january-2026); [FYERS notice](https://fyers.in/notice-board/revision-in-index-derivatives-contracts-lot-size/)
- **Bank Nifty is monthly only.** NSE ended Bank Nifty weeklies in November 2024 (last weekly 13 Nov 2024) after SEBI limited each exchange to one weekly benchmark. NSE kept Nifty 50. Bank Nifty monthly expires on the last Tuesday — [Business Standard: NSE opts for Nifty 50 weekly](https://www.business-standard.com/markets/stock-market-news/nse-opts-for-nifty-50-in-weekly-options-following-sebi-s-benchmark-mandate-124101100903_1.html); [Univest Bank Nifty weekly summary June 2026](https://univest.in/blogs/nifty-bank-summary-for-the-week-22-26-june-2026); [HDFC Securities](https://www.hdfcsec.com/blog/details/derivative-weekly-expiry-contracts-to-be-restricted-to-benchmark-indices)
- Nifty monthly futures expire on the last Tuesday of the month — [Sahi: Nifty futures explained](https://www.sahi.com/blogs/nifty-futures-explained-lot-size-expiry-margin-and-strategy)
- **Sensex lot = 20**, unchanged in 2026, for weekly and monthly options. It was raised from 10 by a BSE notice of 21 Oct 2024. BSE still offers Sensex weekly options — [AlgoTest: Sensex lot size](https://algotest.in/blog/sensex-lot-size.md); [Rupeezy: BSE and NSE lot size changes](https://rupeezy.in/blog/bse-nse-lot-size-changes-for-index-derivatives); [Bigul: no more weekly expiry for BankNifty](https://www.bigul.co/blog/no-more-weekly-expiry-for-banknifty-how-will-it-affect-the-retail-investors)
- **Nifty level:** closed at 22,687.65 on 22 Oct 2026 (−123.70, −0.54%) — [JM Financial market note](https://www.jmfinancialservices.in/market-news-and-insights/1735600). (This is a single source. The October 2026 monthly F&O expiry was 27 Oct 2026.)
- **Nifty futures margin:** illustrative figures only. About ₹1.3–1.6 lakh per lot with Nifty near 24,000 — [Sahi](https://www.sahi.com/blogs/nifty-futures-explained-lot-size-expiry-margin-and-strategy). About ₹1.16 lakh blocked against ≈ ₹15.3 lakh notional at Nifty 23,500 — [OneTradeJournal: SPAN margin](https://onetradejournal.com/glossary/span-margin). Exposure margin for index futures is typically 2–3.5% of contract value on top of SPAN — [OneTradeJournal: exposure margin](https://onetradejournal.com/glossary/exposure-margin)
- **MCX contract specifications and indicative margins** (third-party, prices of 14–17 Oct 2026):

| Contract | Lot | Tick value | Contract value | Indicative margin |
|---|---|---|---|---|
| Gold Mini (GOLDM) | 100 g, quoted per 10 g | ₹1 = ₹10/lot | ≈ ₹14.8 lakh | ₹59k–96k (another source: ₹74k–1.3L) |
| Silver Mini (SILVERM) | 5 kg, quoted per kg | ₹1 = ₹5/lot | ≈ ₹10.6 lakh | ₹42k–69k |
| Crude Oil Mini (CRUDEOILM) | 10 bbl | ₹1 = ₹10/lot | ≈ ₹95,720 | ₹4k–6k (see flag below) |
| Gold Petal | 1 g | – | ≈ ₹14k–15k | ≈ ₹1,420 (at ₹1,41,850/10 g, 3 Aug 2026) |
| Gold Guinea | 8 g | – | – | – |
| Silver Micro (SILVERMIC) | 1 kg | – | – | – |

  Sources: [BhaavBrief: MCX lot sizes 2026](https://bhaavbrief.in/learn/mcx-lot-sizes); [Sahi: commodity margin 2026](https://www.sahi.com/blogs/commodity-margin-lot-size-2026); [AlgoTest: MCX lot size 2026](https://algotest.in/blog/mcx-lot-size/); [Aditya Birla Capital: MCX gold explained](https://www.adityabirlacapital.com/abc-of-money/mcx-gold-trading-explained); [Zerodha Support: commodity options list (GOLD 1 kg, GOLDM 100 g, SILVER 30 kg, SILVERM 5 kg)](https://support.zerodha.com/category/trading-and-markets/trading-faqs/general/articles/how-can-i-trade-commodity-options-in-zerodha)
- Gold margin rule: initial margin is the higher of 6% or SPAN, plus extreme-loss margin of at least 1.25%, and it changes with volatility — [ICICI Direct: trading gold on MCX](https://www.icicidirect.com/ilearn/commodity/articles/how-to-trade-gold-in-commodity-derivatives-market-in-india-1). One source gives Gold Mini NRML margin of ₹1,40,554 at a 9.25% rate (a possible outlier) — [search extract, BhaavBrief/Sahi](https://bhaavbrief.in/learn/mcx-gold-contracts)
- Liquidity: Zerodha warns that liquidity is "quite bad" in MCX gold contracts other than the big Gold and Gold Mini. Gold Ten, Guinea and Petal trade thinly with wide spreads — [Zerodha Varsity: Gold](https://zerodha.com/varsity/chapter/gold-part-1/); [Aditya Birla Capital](https://www.adityabirlacapital.com/abc-of-money/mcx-gold-trading-explained)

### Inferences (arithmetic)
- **Nifty futures notional** = 65 × 22,700 = **₹14,75,500**. Scaling the ₹1.16L-on-₹15.3L ratio (7.6%) gives ≈ ₹1.12 lakh. The ₹1.3–1.6L-at-24,000 range scales to ≈ ₹1.23–1.51 lakh. **Either way, one unhedged Nifty futures lot is ≥ 100% of a ₹1 lakh account.** Even if margin were available, the exposure is 14.75x leverage: a 1% Nifty move (≈ 227 points) = 227 × 65 = ₹14,755 = **14.8% of capital**.
- **Sensex futures/options notional**: Sensex level was not found. At Nifty's usual ratio of about 3.27x, Sensex ≈ 74,000, so 20 × 74,000 ≈ ₹14.8 lakh, similar to Nifty. *(Estimate.)*
- **Bank Nifty**: 30 units × index level. The October 2026 level was not found. At any level near 50,000 the notional would be ≈ ₹15 lakh. From my background knowledge (not re-verified this session), SEBI's October 2024 framework set a minimum index derivative contract value of ₹15 lakh at introduction. That is why all index lots cluster around ₹15 lakh notional.
- **ATM Nifty weekly option premium**: not sourced. Black-Scholes approximation (ATM ≈ 0.4 × S × σ × √T) with S = 22,700, σ ≈ 14%, T = 4/365: 0.4 × 22,700 × 0.14 × 0.1047 ≈ ₹133. I use ₹100 / ₹150 / ₹200 as the range. **One lot at ₹150 = 65 × 150 = ₹9,750 = 9.75% of capital.** At ₹100 it is ₹6,500 (6.5%); at ₹200 it is ₹13,000 (13%). ₹1 lakh can buy at most about 10 lots at ₹150, which would put the whole account into decaying premium.
- **Option selling** (naked) needs futures-like margin (≈ ₹1.1–1.5L/lot), so it is out of reach. Hedged spreads need less, but I found no 2026 figure.
- **MCX on ₹1 lakh:**
  - Gold Mini margin is ₹59k–96k (59–96% of capital). A ₹30/10g move (≈ 0.2%) = ₹300/lot.
  - Silver Mini is ₹42k–69k (42–69%).
  - Crude Mini is the only liquid "mini" that fits comfortably. At 10 bbl × ~₹9,572 ≈ ₹95,720 notional, the account would have ≈ 1x notional exposure per lot. **Flag:** a ₹4–6k margin is only 4–6% of notional, which looks low for a volatile crude market. Confirm on Zerodha's margin calculator.
  - Gold Petal (≈ ₹1.4k margin) and Silver Micro (1 kg ≈ ₹10.6L / 5 = ₹2.12 lakh notional; margin scaled from Silver Mini ≈ ₹8.4k–13.8k, an estimate) fit easily, but liquidity is thin.

### Gaps
- No official NSE/BSE/MCX circular or live margin calculator could be loaded. All margins are third-party estimates.
- Sensex, Bank Nifty and Nifty 500 index levels for late October 2026 were not found. The Nifty level is from one source (22 Oct 2026).
- No live ATM option premium or bid-ask spread data was found. The premium range is a model estimate.
- Gold Guinea and Silver Micro margins were not found, and the Crude Mini margin looks unusually low.

---

## Q3. Worked round-trip cost examples (Zerodha, post-April-2026 rates)

### Takeaway
On explicit charges alone, one round trip costs about **₹70 for a ₹150-premium Nifty option lot, ₹882 for a Nifty futures lot, ₹83 for ₹1 lakh intraday equity, ₹238 for ₹1 lakh delivery, ₹302 for Gold Mini and ₹64 for Crude Mini.** At 2–5 round trips a day, explicit costs alone take **≈ 3–8% of a ₹1 lakh account per month** in options, crude mini or unlevered intraday equity. Gold Mini would take 13–32% a month and Nifty futures 37–93%. Slippage comes on top of these figures.

### Cited Findings
- All rates are as in Q1 (brokerage, STT/CTT, exchange, SEBI, stamp, GST, DP) — [Zerodha charges page](https://zerodha.com/charges/); [Zerodha Support STT](https://support.zerodha.com/category/account-opening/resident-individual/ri-charges/articles/how-is-the-securities-transaction-tax-stt-calculated); [Zerodha DP charges via Finology](https://select.finology.in/articles/broker/dp-charges-in-zerodha)
- Contract values: Nifty 22,687.65 on 22 Oct 2026 — [JM Financial](https://www.jmfinancialservices.in/market-news-and-insights/1735600). Gold Mini ≈ ₹14.8L, Silver Mini ≈ ₹10.6L, Crude Mini ≈ ₹95,720 (17 Oct 2026) — [BhaavBrief](https://bhaavbrief.in/learn/mcx-lot-sizes)

### Inferences (worked calculations; buy and sell at the same price to isolate cost)

Formula: Total = Brokerage(buy + sell) + STT/CTT + Exch% × (buy + sell turnover) + ₹10/cr × turnover + Stamp% × buy + 18% × (brokerage + exchange + SEBI) [+ DP].

**(a) Nifty ATM weekly option, 1 lot (65), buy and sell at ₹150.** Buy turnover = 65 × 150 = ₹9,750; sell = ₹9,750.
- Brokerage 20 + 20 = ₹40.00
- STT 0.15% × 9,750 (sell) = ₹14.63
- NSE txn 0.03553% × 19,500 = ₹6.93
- SEBI 0.0001% × 19,500 = ₹0.02
- Stamp 0.003% × 9,750 = ₹0.29
- GST 18% × (40 + 6.93 + 0.02) = ₹8.45
- **Total ₹70.32 = 0.070% of ₹1L capital = 0.72% of premium deployed. Breakeven = 70.32 / 65 = 1.08 Nifty points.**
- Sensitivity: premium ₹100 → ₹62.61 (0.96 pts); premium ₹200 → ₹78.02 (1.20 pts).
- Sensex equivalent (20 × ₹490 premium, BSE 0.0325%) → ₹69.73, essentially the same.
- Slippage (assumption, not sourced): 0.5 point per side = 65 × 1.0 = ₹65 per round trip, which roughly doubles the cost to **≈ ₹135**.

**(b) Nifty futures intraday, 1 lot, buy and sell at 22,700.** Notional = ₹14,75,500 per side.
- Brokerage min(20, 0.03% × 14.755L = ₹442.65) = ₹20 × 2 = ₹40.00
- STT 0.05% × 14,75,500 = ₹737.75
- NSE txn 0.00183% × 29,51,000 = ₹54.00
- SEBI ₹2.95; stamp 0.002% × 14,75,500 = ₹29.51
- GST 18% × (40 + 54.00 + 2.95) = ₹17.45
- **Total ₹881.67 = 0.88% of ₹1L capital per round trip. Breakeven = 13.56 Nifty points.**
- Under the pre-April-2026 0.02% STT it would have been ₹439.02 (6.75 pts). **The Budget 2026 hike doubled futures round-trip cost.** (This is moot for ₹1L, since margin exceeds capital.)

**(c) ₹1,00,000 intraday equity (MIS), NSE.**
- Brokerage min(20, ₹30) × 2 = ₹40.00
- STT 0.025% × 1,00,000 = ₹25.00
- NSE txn 0.00307% × 2,00,000 = ₹6.14
- SEBI ₹0.20; stamp 0.003% × 1,00,000 = ₹3.00
- GST 18% × 46.34 = ₹8.34
- **Total ₹82.68 = 0.083% of capital.** Breakeven move ≈ 0.083%.
- At 5x MIS leverage (₹5 lakh position): **₹224.61** (0.225% of capital; 0.045% of notional).

**(d) ₹1,00,000 delivery (CNC), NSE, single scrip.**
- Brokerage ₹0
- STT 0.1% × 2,00,000 = ₹200.00
- NSE txn ₹6.14; SEBI ₹0.20; stamp 0.015% × 1,00,000 = ₹15.00
- GST 18% × 6.34 = ₹1.14; DP ₹15.34
- **Total ₹237.82 = 0.238% of capital per round trip.**

**(e) MCX futures, 1 lot each.**
- **Gold Mini (₹14.8L)**: brokerage ₹40 + CTT 0.01% × 14.8L = ₹148 + MCX 0.0021% × 29.6L = ₹62.16 + SEBI ₹2.96 + stamp 0.002% × 14.8L = ₹29.60 + GST 18% × 105.12 = ₹18.92 → **₹301.64 (0.30% of capital); breakeven ≈ ₹30.2 per 10 g.**
- **Crude Mini (₹95,720)**: ₹40 + ₹9.57 + ₹4.02 + ₹0.19 + ₹1.91 + ₹7.96 → **₹63.66 (0.064%); breakeven ≈ ₹6.37/bbl.**
- **Silver Mini (₹10.6L)**: **₹229.44**; breakeven ≈ ₹45.9/kg.
- **Gold Petal (≈ ₹14,800)**: brokerage is 0.03% (₹4.44/side) → ₹13.02 total. Cheap, but illiquid.

**Monthly explicit cost at 2 / 3 / 5 round trips per day × 21 days (as % of ₹1L):**

| Instrument (per RT) | 2 RT/day | 3 RT/day | 5 RT/day |
|---|---|---|---|
| Nifty option ₹150 (₹70.32) | ₹2,953 (2.95%) | ₹4,430 (4.43%) | ₹7,383 (7.38%) |
| + 0.5-pt/side slippage (≈ ₹135.32) | ₹5,683 (5.68%) | ₹8,525 (8.53%) | ₹14,209 (14.21%) |
| Nifty futures (₹881.67) | ₹37,030 (37.0%) | ₹55,545 (55.5%) | ₹92,575 (92.6%) |
| Intraday equity ₹1L (₹82.68) | ₹3,473 (3.47%) | ₹5,209 (5.21%) | ₹8,682 (8.68%) |
| Intraday equity ₹5L (5x) (₹224.61) | ₹9,433 (9.43%) | ₹14,150 (14.15%) | ₹23,584 (23.58%) |
| Delivery ₹1L (₹237.82)* | ₹9,988 (9.99%) | ₹14,983 (14.98%) | ₹24,971 (24.97%) |
| Gold Mini (₹301.64) | ₹12,669 (12.67%) | ₹19,003 (19.0%) | ₹31,672 (31.67%) |
| Crude Mini (₹63.66) | ₹2,674 (2.67%) | ₹4,010 (4.01%) | ₹6,684 (6.68%) |

*Delivery at 2–5 round trips per day is not realistic. For swing trading at 4–8 round trips per month the cost is ₹951–1,903 (0.95–1.9%).
- Add Kite Connect at ₹500/month (0.5% of capital; see Q6).
- The hurdle is lowest for option buying, where brokerage dominates and STT is small in rupees. But costs are 0.6–1% of premium per round trip, so the edge has to be large relative to premium.

### Gaps
- Real slippage and bid-ask data for Nifty weekly ATM options, Crude Mini and Gold Mini were not found. The ₹65/RT slippage is an assumption.
- Income tax is not included. F&O and intraday profits are business or speculative income taxed at slab rates, which reduces net returns further. Not researched here.
- Charges from Zerodha's brokerage calculator could not be cross-checked directly.

---

## Q4. Feasibility math: ₹2,000/day vs 5–7%/month on ₹1,00,000

### Takeaway
**₹2,000/day on ₹1 lakh is 2% per day: 42% per month and 500% per year if profits are withdrawn, or about 14,000% per year (₹1L → ₹1.41 crore) if compounded.** That is roughly 40x the long-run Nifty return and 13x Medallion's reported net return. Even at a world-class Sharpe ratio of 3 it implies ≈ 10.5% daily volatility, which makes ruin close to certain. **5–7% per month (₹238–333/day; 60–84% simple, 80–125% compounded per year)** is still above Medallion's reported net return and well above any Indian fund. It is arithmetically possible with moderate leverage but needs a Sharpe of about 2 to avoid deep drawdowns, and costs alone take 3–6% of capital a month at typical intraday frequency.

### Cited Findings
- Over 91% of individual F&O traders lost money in FY25. Aggregate net loss was ₹1,05,603 crore (vs ₹74,812 crore in FY24) after transaction costs. The average loss was about ₹1.1 lakh per trader (vs ₹86,728). The study covered the top 13 brokers and ~96 lakh traders — [Business Standard: SEBI study FY25](https://www.business-standard.com/markets/news/net-losses-of-traders-in-fo-widens-in-fy25-sebi-study-125070701221_1.html); [Value Research: average trader lost ₹1.1 lakh](https://www.valueresearchonline.com/stories/225398/average-trader-lost-rs-1-1-lakh-fo-fy25/); [NISM](https://www.nism.ac.in/equity-linked-exchange-traded-derivative-contracts-the-retail-rush-and-regulatory-measures/)
- A later SEBI study covering FY25–FY26 found the share of loss-makers rising from ~91% among first-year traders to over 95% among traders with four or more consecutive years — [search extract summarising SEBI follow-up study; Angel One news](https://www.angelone.in/news/market-updates/retail-f-o-losses-rose-to-over-1-lakh-crore-trader-participation-dropped-20-percent) *(I did not open the primary document. Treat as reported.)*
- Unique F&O traders fell about 20% year on year after SEBI's measures — [Business Standard](https://www.business-standard.com/markets/news/individual-investors-shrink-20-percent-fo-segment-125070800801_1.html)

### Inferences (arithmetic)

**Target 1: ₹2,000/day net**
- Daily: 2,000 / 1,00,000 = **2.00%/day**.
- Monthly (21 trading days): simple 21 × 2% = **42%** (₹42,000). Compounded 1.02²¹ = **1.5157 → +51.6%**.
- Annual (≈ 250 trading days): simple 250 × ₹2,000 = ₹5,00,000 = **500%/yr** on fixed ₹1L. Compounded 1.02²⁵⁰ = **141.27x → +14,027%** (₹1L → ₹1.41 crore). With 252 days: 146.97x.
- Required gross per day = net + costs. For Nifty options at 3 RT/day including slippage: 3 × ₹135.32 = ₹406, plus Kite ₹500/21 ≈ ₹24 → **gross ≈ ₹2,430/day ≈ ₹810 per trade ≈ 12.5 option points per lot traded, net of losers** (≈ 8.3% of a ₹150 premium as expectancy on every trade).
- **Required win rate with one lot per trade** (net ₹667/trade + ₹135 cost):
  - Risk ₹650 (10 pts, 0.65% of capital), reward 1:2 (₹1,300): W ≥ (667 + 135 + 650) / (1,300 + 650) = **74.5%**. At 1:1 it is impossible (>100%).
  - Risk ₹1,300 (20 pts, 1.3%), reward ₹2,600: **W ≥ 53.9%** (1:1 needs 80.8%).
  - Risk ₹2,600 (40 pts, 2.6%; 27% of premium), reward ₹5,200: **W ≥ 43.6%** (1:1 needs 65.4%).
  - Sustaining 54–75% win rates at 1:2 reward:risk after costs, every day, is far outside what retail data supports (91% lose).
- **Volatility implied by the target:** daily mean = 2%. Daily Sharpe = annual Sharpe / √250.
  - Sharpe 3 (elite): daily vol = 2% / (3/15.81) = **10.5%** (annual 167%).
  - Sharpe 2: daily vol 15.8% (annual 250%).
  - Sharpe 1: daily vol 31.6%.
  - Nifty's own daily volatility is about 1%, so this needs roughly 10–30x Nifty-equivalent risk. That is consistent with putting the whole account into options, or running 1 futures lot (14.8x).
- **Kelly view (compounding):** log growth needed = 250 × ln(1.02) = 4.95/yr. Maximum Kelly growth ≈ Sharpe² / 2 (continuous-time result, background knowledge), so the required **Sharpe ≥ √(2 × 4.95) = 3.15 even at full Kelly**. At full Kelly, portfolio volatility equals the Sharpe ratio (≈ 315%/yr), and there is roughly a 50% chance of a 50% drawdown at some point (Thorp's full-Kelly result, background knowledge).
- **Losing streaks:** at 3 trades/day ≈ 750 trades/yr and W = 50%, the expected number of streaks of 8 or more losses ≈ 750 × 0.5⁸ × 0.5 ≈ **1.5 per year** (≥6 losses: ≈ 5.9; ≥10 losses: ≈ 0.37). Drawdown from 8 straight losses: at 2% risk/trade **14.9%**; at 5% **33.7%**; at 10% **57.0%**. At W = 60%, ≥8-loss streaks ≈ 0.29/yr. Only aggressive sizing of 5–10% risk per trade can produce 2%/day, and at that sizing a routine streak removes a third to half of the account.

**Target 2: 5–7% per month**
- 5%: ₹5,000/month ≈ **₹238/day** (0.238%/day simple; 0.233%/day compounded). Annual simple 60%, compounded 1.05¹² = **1.796 → +79.6%**.
- 7%: ₹7,000/month ≈ **₹333/day** (0.333%/day; 0.323% compounded). Annual simple 84%, compounded 1.07¹² = **2.252 → +125.2%**.
- **Cost hurdle:**
  - 1 Nifty option RT/day with slippage: 21 × ₹135.32 = ₹2,842 + Kite ₹500 = ₹3,342/month. Gross needed = ₹8,342 (8.3%/month) for 5% net, or ₹10,342 (10.3%) for 7%. Costs are 33–40% of gross.
  - At 2 RT/day: costs ₹6,183, so gross needed is ₹11,183–13,183 (11–13%/month). **Costs exceed the net target.**
  - Low-frequency swing/delivery (4 RT/month): ₹951 + ₹500 = ₹1,451, so gross needed is 6.45–8.45%/month. A much lower hurdle.
- **Volatility at a given Sharpe:**
  - Sharpe 2: annual vol 30–42%, daily 1.9–2.7% (≈ 2–3x Nifty risk).
  - Sharpe 1: annual vol 60–84%, daily 3.8–5.3%.
  - Kelly minimum Sharpe for compounding: 5% needs √(2 × 12 × ln1.05) = **1.08**; 7% needs **1.27**. Those are full-Kelly floors with very large drawdowns. Realistic fractional Kelly needs roughly 1.3–1.5+ (half Kelly growth ≈ 3/8 × S², giving S ≈ 1.25 for 5% and 1.47 for 7%).
- **Bottom line:** ₹2,000/day (42%/month) is 6–8x the 5–7%/month target in raw monthly return. Because of compounding and volatility drag, it is effectively impossible without near-certain ruin. 5–7%/month is "only" extraordinary: about 2–3x Medallion's reported net CAGR on a compounded basis.

### Gaps
- There is no empirical distribution of retail algo strategy Sharpe ratios in India. The SEBI study reports P&L, not risk-adjusted returns.
- The Kelly and full-Kelly drawdown results are standard theory (continuous-time, log-normal returns). Fat tails and gap risk (e.g., expiry-day moves) make real outcomes worse.

---

## Q5. Benchmarks for context

### Takeaway
The best long-run compounding records are ~12–14% (Nifty 50 TRI, 20 years), ~20–22% (the top Indian small-cap mutual fund, 10 years), 19.9% (Berkshire, 60 years) and a reported ~39% net / ~66% gross for Medallion (disputed). **On a simple basis, ₹2,000/day (500%/yr) is ~40x Nifty, ~25x Berkshire and ~13x Medallion net. 5–7%/month (60–84% simple, 80–125% compounded) is 2–3x Medallion net and 4–6x the best Indian MF.**

### Cited Findings
- Nifty 50 TRI 20-year CAGR ≈ **12.44%** (price return ≈ 11.09%), data as of 5 May 2026 — [Bajaj Finserv AMC: Nifty 50 historical returns](https://www.bajajamc.com/knowledge-centre/nifty-50-historical-returns). The same 12.44% is attributed to NSE's Nifty 50 whitepaper (March 2026) — [Holistic Investment](https://www.holisticinvestment.in/nifty-50-prediction-2030-2035-2040-2045/). That source also claims 20-year rolling returns briefly fell into single digits during a 2026 sell-off (single source, unverified).
- An earlier window (April 2025): Nifty 50 TRI 10y 11.7%, 15y 12.4%, 20y 14.4% — [Cafemutual citing FundsIndia](https://cafemutual.com/news/industry/34531-indian-equities-have-outperformed-all-other-asset-classes-over-the-long-term). Rolling 20-year TRI CAGRs ranged from 10.57% (2000–2020) to 17.05% (2003–2023) — [Value Investing newsletter](https://value-investing.beehiiv.com/p/nifty-50-cagr-last-20-years)
- Top Indian equity MF over 10 years: Nippon India Small Cap ≈ **20.6–22.1% CAGR** (Kuvera 20.61% lump sum; Tradebrains 22.1%; Rupeezy 21.88% as of Nov 2024). Quant Small Cap ≈ 19.9% — [Kuvera](https://kuvera.in/blog/which-mutual-funds-have-the-highest-returns-over-the-last-10-years-in-india/); [Tradebrains](https://tradebrains.in/money/top-5-mutual-funds-that-could-turn-30000-monthly-sip-into-1-crore-in-10-years/); [Rupeezy](https://rupeezy.in/blog/highest-return-mutual-fund-in-last-10-years). These are the most volatile categories.
- Berkshire Hathaway: **19.9%** compounded annual gain 1965–2024 vs 10.4% for the S&P 500 (with dividends); total gain 5,502,284% — [NBC/CNBC: Buffett's return tally after 60 years](https://www.nbcdfw.com/news/business/money-report/warren-buffetts-return-tally-after-60-years-5502284/3832965/); [Statista](https://www.statista.com/chart/amp/34413/how-berkshire-hathaway-outperformed-the-market-over-60-years)
- Renaissance Medallion: reported ~**66%** average annual gross and ~**39%** net of fees, 1988–2018 (from Zuckerman, *The Man Who Solved the Market*) — [The Wealth Advisor/Business Insider](https://www.thewealthadvisor.com/article/how-secretive-hedge-fund-keeps-beating-buffett-year-after-year); [HedgeFundAlpha](https://hedgefundalpha.com/strategies/renaissance-medallion-fee-structure/). **Contested:** an arXiv paper argues that compounded pre-fee returns were probably below 35% once fund-size changes are accounted for — [arXiv 2405.10917](https://arxiv.org/pdf/2405.10917v2). Sources also conflict on the fee (5% + 44% vs 5% + 30%).

### Inferences
- Multiples on a simple annual basis:
  - ₹2,000/day = 500% ÷ 12.4% (Nifty TRI) ≈ 40x; ÷ 19.9% (Berkshire) ≈ 25x; ÷ 39% (Medallion net) ≈ 13x.
  - 5–7%/month compounded (79.6–125.2%) ÷ 39% ≈ 2.0–3.2x Medallion net; ÷ 21% (top MF) ≈ 3.8–6.0x; ÷ 12.4% ≈ 6.4–10x Nifty TRI.
- A more realistic "excellent" target for a ₹1L systematic account is index-plus-a-few-points: 15–25%/yr ≈ ₹15–25k/yr ≈ ₹60–100/day. At that scale a fixed ₹6,000/yr Kite Connect fee alone takes 24–40% of profit.

### Gaps
- Nifty 500 long-run CAGR was not found in this session.
- Specific Indian PMS or quant-fund (AIF/PMS) multi-year returns were not found. Use APMI or PMS Bazaar data if needed.
- 2025 year-end Berkshire and 2026 YTD index returns were not confirmed.

---

## Q6. Kite Connect API and historical data pricing

### Takeaway
**Order and account APIs are free (Kite Connect "Personal"). The data APIs (real-time WebSocket plus historical candles) cost ₹500 per app per month, down from ₹2,000.** Historical data has had no separate add-on fee since 8 Feb 2025. For a ₹1L account, ₹500/month is 0.5% of capital a month (6% a year). That is a meaningful hurdle by itself, roughly equal to half a year of Nifty's long-run return.

### Cited Findings
- Kite Connect data API fee (real-time and historical) cut to **₹500/month from ₹2,000**, citing NSE's circular on operational specifications for retail algo trading. Order placement and account management APIs have been free since March 2025. Static IP is required only for order place/modify/cancel endpoints. No refunds for past payments — [kite.trade forum: Revising Kite Connect fees from ₹2000 to ₹500 per month](https://kite.trade/forum/discussion/comment/49590); [kite.trade forum comment](https://kite.trade/forum/discussion/comment/49597)
- Historical data add-on (previously an extra ₹2,000/month) has been free with the base Kite Connect subscription since **8 Feb 2025** — [kite.trade forum: Historical data is now free](https://kite.trade/forum/discussion/14806/historical-data-is-now-free)
- A third-party check dated 14 Oct 2026 lists Kite Connect Personal at ₹0 and Connect at ₹500 per app per month. It notes the pricing pages don't state whether GST is included — [OneTradeJournal: Kite Connect Personal vs Connect](https://onetradejournal.com/trading-apis/kite-connect-personal-vs-connect)
- **Conflict:** Zerodha's support article still says "₹2000 per app each month" with free historical data. It appears not to have been updated — [Zerodha Support: charges for Kite APIs](https://support.zerodha.com/category/trading-and-markets/kite-api/articles/what-are-the-charges-for-kite-apis)

### Inferences
- Annual data cost = ₹500 × 12 = ₹6,000 (₹7,080 if 18% GST applies). That is 6–7.1% of ₹1L capital per year, or ≈ ₹24–28 per trading day.
- An algo that only places orders (using free data from elsewhere, or computing signals from Kite's free order/portfolio endpoints) can avoid the fee, but most intraday algos need the tick feed.
- Under the NSE/SEBI retail algo framework, the static-IP requirement for order endpoints may add a small VPS or static-IP cost. *(No figure found.)*

### Gaps
- Whether ₹500 includes GST is unresolved.
- The exact date of the ₹2,000 → ₹500 cut was not visible in the search extract. It followed NSE's retail-algo operational circular (2025).
- Rate limits and historical-data depth limits were not re-verified this session.
