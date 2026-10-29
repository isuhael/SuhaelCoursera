# Evidence on Retail and Algo Options Strategies in Indian Index Options (Nifty, Bank Nifty, Sensex, Fin Nifty): Performance and What Still Works After SEBI's 2024–2026 Changes

Current as of 2026-10-29.

**How this research was done.** Fetching full pages was blocked in this session for sebi.gov.in, tradingqna.com and quantsapp.com (DNS failures under the session's network policy), so I could not read them in full. Every finding below therefore comes from web-search result summaries of the cited pages, not from reading the full documents. Exact figures, especially from the SEBI PDFs, should be checked against the primary documents before publication.

Labels used throughout:
- **[PRE]**: evidence from before the November 20, 2024 SEBI changes.
- **[POST]**: evidence from after them.
- **[SPAN]**: a dataset or test that straddles both periods.

---

## 1. Intraday option buying (ORB, momentum/breakout buying, expiry-day "hero-zero"): win rate, expectancy, drawdowns, persistence after costs

### Takeaway
Regulator data shows option buying is where most retail losses happen, both before and after the 2024 changes. Some backtests do show positive expectancy for rule-based intraday buying (for example, Zerodha's ORB test from 2022 to Feb 2026). But their win rates are below 50%, the edge decayed from 2024 to 2025, and none is an independent audited live record. Expiry-day "hero-zero" buying of very cheap OTM options shows negative expectancy in the one recent rule-based backtest found.

### Cited Findings
**Regulator and academic data on retail option buying**
- [POST] SEBI's FY26 study (released Aug 20, 2026): 87.7% of individual traders had net losses in FY26 (vs 90.9% in FY25), and about 92% of aggregate individual losses came from options trading — [Tribune](https://www.tribuneindia.com/news/business/nearly-9-in-10-individual-derivatives-traders-lost-money-in-fy26-losses-hit-rs-91685-crore-despite-fall-in-participation-sebi/); [BusinessToday](https://www.businesstoday.in/markets/story/rs91685-cr-lost-88-of-individual-traders-lost-money-in-fy26-options-drove-92-of-losses-550474-2026-08-21)
- [POST] Before transaction costs, 82.1% of individuals lost money in FY26; after costs the figure is 87.7%. Costs alone turn about 5.6% of traders from winners into losers — [Finnovate](https://www.finnovate.in/learn/blog/sebi-fno-trader-losses-fy26-individual-derivatives)
- [POST] Secondary coverage of the FY26 study says about 97% of individual traders were predominantly option buyers and only about 2% were mainly option sellers. This comes from a broker blog and is not verified against the PDF — [Riddhi Siddhi Share Brokers](https://www.riddhisiddhisharebrokers.com/sebi-fo-traders-loss-study-fy26)
- [POST] The same secondary coverage gives a 91.9% loss rate for traders under 30 (single secondary source) — [Open Magazine](https://openthemagazine.com/business/sebi-fo-loss-study-explained-why-9-in-10-retail-traders-lost-91685-crore-in-fy26)
- [PRE] SEBI's FY22–FY24 study: 93% of individual F&O traders lost money, with aggregate losses above ₹1.8 lakh crore, and only 7.2% made a profit over the three years — [Business Standard](https://www.business-standard.com/markets/capital-market-news/sebi-study-exposes-massive-losses-for-individual-f-o-traders-in-india-124092400948_1.html); [News On AIR](https://www.newsonair.gov.in/sebi-study-reveals-individual-traders-face-severe-losses-in-equity-fo-segment)
- [PRE] SEBI's January 2023 study: 89% of individual F&O traders lost money in FY22 — [Business Standard](https://www.business-standard.com/amp/article/markets/sebi-study-suggests-89-retail-traders-in-equity-f-o-suffered-losses-123012501466_1.html)
- [PRE/SPAN] Academic working paper "Animal Spirits on Steroids: Evidence from Retail Options Trading in India" (Agarwal, Ghosh, Prabhala, Zhao; CFR working paper 25-09; AEA 2026). It uses market-wide NSE retail trade data. Key findings:
  - Retail activity concentrates in index options: 75% of retail premium and 93% of retail notional.
  - Trading is dominated by day trades and short-duration directional bets.
  - Activity rises from 5 days before expiry and surges at 0DTE. Retail reached 42% of 0DTE volume by the end of the sample.
  - Estimated retail losses are INR 506 billion (about $6.3bn).
  - FinTech-broker users trade more, hold for shorter periods and lose more.
  - When costs rose, traders shifted to cheaper options, with worse outcomes. — [CFR Cologne WP](https://www.cfr-cologne.de/download/workingpaper/cfr-25-09.pdf); [AEA program](https://www.aeaweb.org/conference/2026/program/paper/StD8aadb); [U Alberta copy](https://www.ualberta.ca/en/finance-department/media-library/documents/vikas-agarwal.pdf)
- [PRE/SPAN] The same paper finds entry into options is more likely after poor stock-market performance and after exposure to lottery-like stocks. The authors read this as speculative behaviour rather than rational learning — [IDEAS/RePEc](https://ideas.repec.org/p/zbw/cfrwps/327125.html)

**Opening Range Breakout (ORB)**
- [SPAN] Zerodha "In The Money" newsletter, ORB on Nifty options (Part 2). The test:
  - Buys strikes priced near ₹200 at 9:16 and uses the 9:15–11:15 premium range as the breakout reference.
  - Takes at most one CE and one PE trade per day, with a 20% stop-loss on premium.
  - Covers Jan 2022–Feb 2026, net of brokerage and taxes, with 0.2% slippage, on about ₹7.5L capital (5 lots × about ₹1.5L).

  Results:
  - Win rate about 48%.
  - The equity curve was smooth until about Jan 2024, then got bumpy, and it had not fully recovered from a drawdown that began in mid-2024.
  - 2022–2024 were "reasonably good", 2025 was "rough" and 2026 has been "decent" so far.
  - Both the buying and the selling ORB variants showed positive expectancy, and selling improved the win rate only marginally. — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/how-to-trade-opening-range-breakout)
- [SPAN] Intraday Lab ran a 30-minute ORB on the Nifty 50 index, not options, with costs not stated. Over 8+ years and 2,122 trades it had a 48.7% win rate and a 1.23 profit factor. The edge came from payoff asymmetry: about +2R average winner vs −1R loser — [Intraday Lab](https://intradaylab.com/blog/nifty-orb-breakout-strategy-backtest)
- One Trade Journal claims an ORB return of 3.5% a month with a 58% win rate on Nifty but gives no methodology. Treat it as low-confidence marketing — [One Trade Journal](https://onetradejournal.com/strategies/opening-range-breakout)

**Expiry-day "hero-zero" / penny options**
- [POST] QuantsApp prebuilt backtest, Oct 2025–Sep 2026. Rule: on Nifty expiry day, buy an OTM option priced under ₹10 after an afternoon range breakout, with no stop. Result: 19 trades, 16% win rate, profit factor 0.51, −₹6,193 before costs and −₹6,994 after costs. The sample is small, and QuantsApp is a platform vendor — [QuantsApp](https://www.quantsapp.com/backtesting/strategies/expiry-day-hero-zero-otm-buy)
- [POST] Zerodha's "Should you trade Penny Options?" uses a "turkey" analogy for far-OTM options priced at ₹1–2: many small, steady outcomes, then one catastrophic one. Its example is an April 2025 Nifty ₹2 call sitting 2,700 points (12.35%) above spot two days before expiry. The article gives illustrations, not a performance record — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/should-you-trade-penny-options)
- A widely quoted claim that "85% of OTM options expire worthless", attributed to a "Derivatives Analysis Institute" study, could not be verified and is not India- or expiry-specific — [Strike.money](https://www.strike.money/options/expiry) (reported claim; unverified)
- Zerodha warns that expiry-day option prices can drift out of line with spot near the close, so apparent arbitrage or "easy money" is often illusory — [Zerodha on X](https://x.com/zerodhaonline/status/1828725615090159867)

### Inferences
- Both the population data (more than 90% of individuals losing for five straight years, with options buying about 92% of losses) and the one academic market-wide study point to negative expectancy for typical retail option buying. That holds before and after November 2024.
- The best-documented intraday-buying "edge" is Zerodha's ORB test, which has a win rate below 50% and depends on rare large winners. Its performance degraded from mid-2024 through 2025, which overlaps both lower realized volatility and the regulatory changes. The data cannot separate the two causes.
- The rule changes raised the cost per trade: lot sizes about 3× larger in Nov 2024, upfront premium and so on. The Animal Spirits paper's finding that traders shift to cheaper, deeper-OTM options when costs rise suggests the changes may have pushed some buyers toward exactly the low-delta lottery trades that test worst. This is an inference, not a measured post-2024 result.
- Hero-zero has negative expectancy in the one rule-based test found (profit factor 0.51). No credible evidence of persistent profitability was found.

### Gaps
- I found no independent, audited live track record, or peer-reviewed paper, showing persistent after-cost profitability for intraday option buying on Indian indices.
- The full ORB article (max drawdown, CAGR, expectancy per trade) could not be read. Only snippet-level figures are available.
- I found no rigorous dataset on how often far-OTM Nifty/Sensex expiry-day options finish worthless. That would need NSE/BSE bhavcopy analysis.
- The ~97% "option buyers" share and the under-30 loss rate are from secondary coverage and need checking against the SEBI FY26 PDF ([sebi.gov.in](https://www.sebi.gov.in/sebi_data/attachdocs/aug-2026/1787233506209.pdf)), which could not be fetched.

---

## 2. Option selling (short straddles/strangles, 9:20 straddle, iron condors/flies, expiry-day selling, positional strangles): the volatility risk premium, returns, drawdowns, tail events

### Takeaway
Academic studies agree that Nifty options carry a positive volatility/variance risk premium (implied volatility above subsequently realized volatility on most days). One peer-reviewed study finds the premium is mainly compensation for overnight risk, which an intraday 9:20 straddle does not hold. Public backtests of popular selling strategies are mixed. For Oct 2025–Sep 2026, platform backtests show several popular structures negative after costs. The tail is real: an academic estimate finds a single COVID-period loss wiped out all of retail's cumulative option-writing gains.

### Cited Findings
**The volatility/variance risk premium (VRP) in Nifty options**
- "Dynamics of variance risk premium: Evidence from India" (International Review of Economics & Finance, vol. 70, 2020). It compares intraday realized variance with model-free implied variance and tests synthetic variance swaps. It finds variance risk is priced in Indian index options and notes the market is retail-dominated — [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S1059056020301222); [IDEAS](https://ideas.repec.org/a/eee/reveco/v70y2020icp321-334.html)
- Bhat (2024), "The asymmetry in day and night option returns: Evidence from an emerging market" (Journal of Futures Markets), finds a day–night asymmetry in short Nifty option returns. The VRP earned by option sellers is mainly compensation for overnight risk — [Wiley](https://onlinelibrary.wiley.com/doi/10.1002/fut.22512?af=R)
- Garg & Vipul (2015), "Volatility Risk Premium in Indian Options Prices" (Journal of Futures Markets, 35(9)), is an earlier journal study. I saw it only in a reference list, so its findings are not confirmed here — [UWasa reference list PDF](https://sites.uwasa.fi/mfjuva/wp-content/blogs.dir/4/files/sites/231/2025/02/MJ0p1cq0ps1gbh7t9f610n515armrk4.pdf)
- A 2025 paper in "Economic Sciences" reports a positive average VRP on Nifty options (implied variance above realized) and highlights tail-loss risk for volatility sellers in turmoil. The journal's quality is uncertain — [Economic Sciences](https://economic-sciences.com/index.php/journal/article/download/356/299/644)
- [SPAN] Agarwal (2026), "The Variance Risk Premium in Nifty 50: A Structural Anatomy Across Nine Empirical Filters", is an SSRN working paper using one-minute option data from Aug 2022 to Mar 2026. It is not peer-reviewed, and its results were not retrieved — [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6530119)
- A non-peer-reviewed GitHub study compares India VIX with subsequent 21-day Nifty realized volatility. The average premium is about 2.46 vol points, it is positive on about 80% of days, and the worst reading was −64.5 vol points on 2020-03-05 (COVID onset). It ignores costs and margin — [GitHub](https://github.com/RajolKumar2003/volatility-risk-premium-india)

**Tail events**
- [PRE] COVID, March 2020:
  - Animal Spirits paper: some retail investors running short-volatility strategies took losses as VIX rose in early March 2020. They reduced but did not close short puts into the March 26, 2020 expiry.
  - The authors estimate a loss of ₹11 billion during COVID that wiped out all cumulative retail gains from options writing. — [Animal Spirits (U Alberta copy)](https://www.ualberta.ca/en/finance-department/media-library/documents/vikas-agarwal.pdf)
- [PRE] COVID market context:
  - The Nifty fell from about 12,430 (late Jan 2020) to about 7,511 (Mar 24, 2020).
  - On Mar 13, 2020 it opened about 5% lower and hit the 10% lower circuit within five minutes (45-minute halt), then swung to more than 3% up within two hours. That kind of whipsaw triggers stops on both legs of a short straddle. — [Business Standard](https://www.business-standard.com/amp/article/markets/short-sellers-caught-off-guard-as-market-swings-within-hours-of-opening-120031301418_1.html); [Strasmore](https://www.strasmore.com/blog/covid-crash-march-2020)
- [PRE] Trader accounts (Zerodha forum) say some option sellers in March 2020 saw option values exceed their margin, lost their whole deposit and owed more at square-off. India VIX spiked above 80. This is anecdotal; I could not read the page itself — [TradingQnA thread](https://tradingqna.com/t/what-happened-with-options-trader-in-march-2020/96234); [One Trade Journal](https://onetradejournal.com/glossary/market-crash)
- [PRE] June 4, 2024 (election results day):
  - The Nifty closed down 5.93% at 21,884.50, with an intraday low of 21,281, about 8.5% below the prior close. The Sensex fell 5.74% after a drop of more than 6,200 points intraday. — [Business Standard](https://www.business-standard.com/markets/news/stock-market-live-updates-june-4-sensex-nifty-lok-sabha-election-results-2024-psu-stocks-nse-124060400081_1.html)
  - India VIX went from 20.94 to 26.75 at the close, after 31.71 intraday. ICICI Direct gives +23.65% to 25.89, so the sources differ slightly. — [NiftyScanner](https://niftyscanner.in/labs/option-premium/2024-06-04/); [ICICI Direct](https://www.icicidirect.com/futures-and-options/news/nifty-june-futures-trade-at-premium/1518821)
  - The Nifty 23,250 put expiring June 6 went from ₹171.45 to ₹1,362.50 (about 8×) between the June 3 and June 4 closes. A short-put or short-strangle seller would have lost roughly 1,190 points per unit on that leg. — [NiftyScanner](https://niftyscanner.in/labs/option-premium/2024-06-04/)
  - The Nifty recovered about 6.4% between June 4 and June 7. — [Vimista](https://vimista.com/stories/business-cycles/june-2024-election-result-sell-off-nifty-sensex/)

**Backtests of popular selling strategies**
- [SPAN] Zerodha "In The Money", Nifty 9:20 straddle episode: one ATM straddle at 9:20 with a fixed 20% stop-loss per leg, held to 3:20. The tests are net of ₹20 per order, statutory costs and 0.25% slippage per leg. The Nifty results themselves were not retrievable — [In The Money by Zerodha (Sensex 0DTE post)](https://inthemoneybyzerodha.substack.com/p/sensex-0dte-straddle-or-strangle)
- [POST] The same newsletter's Sensex 0DTE test: a single 9:20 entry with six lots had a return-to-max-drawdown of 0.64. Spreading six one-lot entries through the day raised it to 2.56. Staggered entries greatly reduce path risk — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/sensex-0dte-straddle-or-strangle)
- [POST] Zerodha's position-sizing series (Feb 2026) estimates margin for a 0DTE Nifty short straddle at about ₹3–3.25 lakh. It also shows that the same set of trades can produce very different drawdowns depending on their order — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/position-sizing-part-3-sizing-option)
- [SPAN] Zerodha's 45 DTE test, about seven years of Nifty data. It sold ATM straddles and 30-delta and 16-delta strangles about 45 days to expiry, with a 50% profit target and a stop at 200% of credit.
  - Five of seven full years were profitable.
  - The 16-delta strangle produced the lowest total points and the most stop-losses, with similar drawdown.
  - A VIX filter pushed strangle win rates to about 85%. — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/we-backtested-the-famous-45-dte-strategy)
- [POST] QuantsApp prebuilt Nifty backtests, Oct 1, 2025–Sep 30, 2026 (platform vendor; one-year samples):
  - 9:20 short strangle: −₹3,054 before costs, max drawdown ₹36,041. The search summary did not show which QuantsApp page this came from. The linked "Straddle-Width Strangle" page is the closest match returned, but the attribution is uncertain. — [QuantsApp (attribution uncertain)](https://www.quantsapp.com/backtesting/strategies/straddle-width-strangle)
  - 9:20 straddle with stop-and-reverse: −₹40,794 before costs, −₹1,09,914 after costs. — [QuantsApp](https://www.quantsapp.com/backtesting/strategies/short-straddle-sl-flip-to-long-leg)
  - Overnight short straddle (close to open): +₹24,344 before costs but −₹3,372 after ₹20 per order and bid-ask slippage. — [QuantsApp](https://www.quantsapp.com/backtesting/strategies/overnight-short-options-close-to-open)
  - 45-DTE monthly short straddle: 13 trades, 54% win rate, profit factor 0.81, −₹29,776 before costs, max drawdown about ₹1.15 lakh. Average losses were larger than average wins. — [QuantsApp](https://www.quantsapp.com/backtesting/strategies/monthly-short-straddle-45dte-50pt-21dte)
- [PRE] TradingTick reports a 68% win rate for Nifty expiry-day straddles over 2020–2024. Methodology and costs are unclear; low-confidence — [TradingTick](https://tradingtick.in/nifty/option-backtesting/nifty-short-straddle-strategy-backtest-results.php)
- [PRE] Practitioner commentary says the Bank Nifty 9:20 straddle weakened in 2022–2023:
  - Lower volatility in 2023 meant fewer opportunities, and a 10:30 entry reportedly did better than 9:20.
  - Mid-day illiquidity leaves SL-M stop orders vulnerable to "stop hunting".
  - Another educator reports a "flat" year attributed to changing dynamics since 2022. — [Marketcalls](https://www.marketcalls.in/futures-and-options/is-the-920-straddle-no-more-working.html); [Marketcalls (gaming)](https://www.marketcalls.in/futures-and-options/how-the-9-20-intraday-straddlers-are-being-gamed.html); [Trade4Wealth](https://trade4wealthtradingacademy.com/920-short-straddle-strategy/) (educator with a course to sell)
- [POST] Counterpoint: a Zerodha forum post titled "Reports of the death of 920 Short Straddle are greatly exaggerated" simulated a plain Nifty 9:20–3:15 straddle for Dec 2024 and showed mostly small gains with one small loss. It covers only one month — [TradingQnA](https://tradingqna.com/t/reports-of-the-death-of-920-short-straddle-are-greatly-exaggerated/179061)
- An individual's Medium post claims an "optimized" 9:20 straddle returns "more than 80% annually" in AlgoTest. Parameter optimization without out-of-sample testing makes this a textbook overfitting risk — [Medium](https://medium.com/@amit179.iitk2/optimized-920-straddle-strategy-to-get-more-than-80-return-annually-e977453dca80)

### Inferences
- The Indian index-option VRP is real and documented in peer-reviewed work. Retail sellers do not automatically collect it:
  - Bhat (2024) implies intraday-only selling such as the 9:20 straddle, which is flat by 3:15, collects little of the premium, because the premium is mostly paid for overnight risk.
  - The overnight-straddle backtest is consistent with that: positive before costs, but costs erased it in Oct 2025–Sep 2026.
- Lot-size increases and the 2% expiry-day ELM raise margin per unit of premium collected (see Q3). So even an unchanged gross edge yields a lower return on margin after Nov 2024.
- Tail risk dominates outcomes. One estimate has retail option writers' cumulative gains wiped out by the COVID loss. On June 4, 2024, a near-ATM put repriced about 8× in a day. Hedged structures (iron condors/flies) and staggered entries limit this; naked positional strangles do not.
- Credible annual return-on-margin figures with full costs and live fills are essentially absent from the public record. Most numbers are broker-newsletter or vendor backtests.

### Gaps
- I found no peer-reviewed study reporting annual return on margin or maximum drawdown for retail-style short straddles or iron condors on Nifty after Nov 2024.
- I found no quantified estimate of aggregate option-seller losses on June 4, 2024.
- The full Zerodha 9:20 straddle and 45 DTE result tables (CAGR, max drawdown) and the Agarwal (2026) SSRN results could not be retrieved.
- I found no study separating the VRP earned by retail vs institutional sellers after the 2024 changes.

---

## 3. Impact of SEBI's November 2024 changes and 2025–2026 changes on strategy viability, capital requirements, expiry-day volumes and premium-selling returns

### Takeaway
The November 2024 package cut notional and contract volumes sharply (about 40% in early December 2024) and reduced the expiry-day share of trading. Premium turnover held up much better, and individual losses fell only modestly. FY25 losses rose about 41%, and FY26 net losses fell to about ₹91,685 crore with 87.7% still losing. Capital requirements per position roughly tripled in Nov 2024 and were trimmed slightly by the 2025–26 lot-size cuts. Liquidity fell again after the July 2025 Jane Street order.

### Cited Findings
**The November 2024 package (SEBI circular, Oct 1, 2024)**
- Effective Nov 20, 2024, new index derivative contracts must have a value of at least ₹15 lakh at introduction, with lots kept in a ₹15–20 lakh band. The old minimum is reported variously as ₹5 lakh or ₹5–10 lakh — [Business Standard](https://www.business-standard.com/amp/markets/news/sebi-announces-six-key-changes-to-curb-speculation-in-derivatives-trading-124100101316_1.html); [Angel One](https://www.angelone.in/news/market-updates/sebi-strengthens-index-derivative-rules)
- Each exchange may offer weekly expiry on only one benchmark index: Nifty on NSE, Sensex on BSE. Bank Nifty and Fin Nifty weeklies were discontinued — [Business Standard](https://www.business-standard.com/amp/markets/news/new-f-o-rule-to-come-into-effect-from-thursday-nov-21-here-s-what-changes-124112000292_1.html); [AlgoTest blog](https://algotest.in/blog/all-index-expiry-day/)
- A 2% Extreme Loss Margin applies on expiry day to all short options open at the start of the day and to short options opened that day which expire the same day. ELM is calculated on contract value (strike × lot size) — [Arihant Capital](https://blog.arihantcapital.com/sebi-tightens-the-reins-introduces-6-new-measures-for-fo-trading/); [BusinessToday](https://www.businesstoday.in/markets/story/sebis-new-fo-rules-kick-off-today-heres-what-are-these-changes-454352-2024-11-20)
- Further phases:
  - Calendar-spread margin benefit removed for contracts expiring that day, and upfront option-premium collection, both effective Feb 1, 2025.
  - Intraday monitoring of position limits from Apr 1, 2025. — [Arihant Capital](https://blog.arihantcapital.com/sebi-tightens-the-reins-introduces-6-new-measures-for-fo-trading/); [Jainam](https://www.jainam.in/blog/sebi-new-rules-for-fo-trading/)

**2025–2026 changes**
- [POST] Lot sizes revised under NSE circular NSE/FAOP/70616: Nifty from 75 to 65 and Bank Nifty from 35 to 30. The first Nifty weekly at 65 expired Jan 6, 2026, and the first monthly Jan 27, 2026 — [5paisa](https://www.5paisa.com/blog/index-derivatives-new-lot-sizes-nse-update-january-2026); [Ventura](https://www.venturasecurities.com/news/stocks/nse-revises-lot-sizes-for-nifty-bank-nifty-derivatives-new-contract-specifications-effective-from-december-30/); [Flattrade](https://flattrade.in/kosh/nse-revises-derivatives/)
- [POST] NSE also revised Bank Nifty and Midcap Select lot sizes in March 2025 — [Business Standard](https://www.business-standard.com/amp/markets/capital-market-news/nse-revises-market-lot-sizes-for-nifty-bank-nifty-midcap-select-f-o-contracts-125033100440_1.html)
- [POST] Expiry-day swap after SEBI limited weekly expiries to Tuesdays and Thursdays:
  - Nifty weekly moved from Thursday to Tuesday, with the first Tuesday expiry on Sep 2, 2025.
  - Sensex moved from Tuesday to Thursday, first on Sep 4, 2025.
  - Nifty monthly contracts now expire on the last Tuesday, and the schedule was still in place in mid-2026. — [Business Standard](https://www.business-standard.com/amp/markets/news/nse-bids-adieu-to-thursday-expiry-as-dates-swap-come-into-effect-explained-125082800635_1.html); [BusinessToday](https://www.businesstoday.in/amp/markets/stocks/story/nse-bse-fo-expiry-days-what-has-changed-for-stock-investors-history-more-480781-2025-06-18)
- [POST] Delta-based (future-equivalent) open interest, SEBI circular of May 29, 2025. Index-option limits:
  - End-of-day net limit of ₹1,500 crore and gross limit of ₹10,000 crore per side, phased in July–Dec 2025.
  - Intraday net limit of ₹5,000 crore per entity from Oct 1, 2025 (Sep 1, 2025 circular), checked through at least four random snapshots, one of them between 2:45 and 3:30 pm. This came after the Jane Street case. — [Business Standard](https://www.business-standard.com/amp/markets/news/sebi-stricter-intraday-position-limits-options-market-regulation-125090200971_1.html); [Outlook Business](https://www.outlookbusiness.com/markets/sebi-shakes-up-derivatives-game-with-new-rules-for-measuring-open-interest-mwpl)
- [POST] A pre-open session was extended to F&O from Dec 6, 2025 (secondary blog) — [Vilasa](https://vilasatrade.com/blog/sebi-margin-and-fo-rules-2026)
- [POST] In Sep 2025 there were media reports that SEBI might consult on ending weekly F&O contracts. I found no evidence that such a paper was issued, and weekly Nifty and Sensex expiries continued into 2026 — [Business Standard](https://www.business-standard.com/markets/news/bse-angel-one-drop-up-to-5-pc-on-report-of-curbs-on-weekly-derivatives-sebi-125091100512_1.html)
- [POST] Sep 2026: a reported SEBI consultation on the closing auction session proposes blending the last 30 minutes of continuous trading with a closing auction to set expiry-day settlement prices, against keeping the 30-minute VWAP. This is unverified secondary reporting — [IndiaIPO](https://www.indiaipo.in/news/detail/sebi-proposes-blended-method-for-derivatives-expiry-pricing)
- [POST] SEBI's retail algo framework (circular of Feb 4, 2025):
  - "White box" (disclosed-logic) algos must be registered with exchanges.
  - "Black box" algo providers must register as Research Analysts and keep a research report for each strategy.
  - Brokers act as principals and algo providers as their agents.
  - Implementation was deferred more than once, and later broker material refers to rules effective April 2026. — [Zerodha Z-Connect](https://zerodha.com/z-connect/business-updates/explaining-the-latest-sebi-algo-trading-regulations); [Tradejini](https://www.tradejini.com/blogs/what-sebis-new-algo-trading-rules-mean-for-you); [AlgoBulls](https://algobulls.com/blog/industry-insights-and-updates/sebi-new-algotrading-regulations-for-retail-investors-2026)

**Volume effects**
- [POST] NSE index-option notional average daily turnover fell from ₹357 trillion (first week of Nov 2024) to ₹207 trillion (first week of Dec 2024), about −42%. BSE fell from ₹104 trillion to ₹80 trillion. NSE index-option contracts fell about 38%. Premium turnover stayed roughly steady — [Outlook Business](https://www.outlookbusiness.com/markets/sebis-regulatory-changes-have-minimal-impact-on-option-premium-turnover); [Business Standard](https://www.business-standard.com/amp/markets/news/derivatives-volumes-crash-37-in-dec-as-sebi-tightens-trading-norms-124122600761_1.html)
- [POST] Notional daily options value fell about 35%, from $5 trillion (Nov 2024) to $3.2 trillion (Feb 2025), but only about 15% in premium terms. The share of 0DTE trades fell to 50% of volumes from 70% — [Business Standard column](https://www.business-standard.com/amp/opinion/columns/sebi-proposals-seek-orderly-conduct-in-f-o-market-amid-volatility-125032401438_1.html)
- [POST] SEBI study (July 2025) comparing Dec 2024–May 2025 with the same period a year earlier:
  - Index-option turnover fell 9% in premium terms and 29% in notional terms, but was still up 14% (premium) and 42% (notional) on two years earlier.
  - Unique individual traders fell about 20%.
  - Individuals' premium turnover fell 11% year on year, though it was up 36% over two years. — [Business Standard](https://www.business-standard.com/amp/markets/news/net-losses-of-traders-in-fo-widens-in-fy25-sebi-study-125070701221_1.html); [The Week/PTI](https://www.theweek.in/wire-updates/business/2025/07/07/dcm92-biz-sebi-derivatives-study.html); [TaxGuru](https://taxguru.in/sebi/sebi-releases-study-equity-derivatives-trends.html)
- [POST] Secondary coverage of SEBI's FY26 study says expiry-day trading was about 70% of index-option turnover in FY25 and about 59% in FY26. The specific outlet could not be pinned down from the search summary; verify in the SEBI PDF — [SEBI FY26 profitability study PDF](https://www.sebi.gov.in/sebi_data/attachdocs/aug-2026/1787233506209.pdf) (via secondary coverage such as [Open Magazine](https://openthemagazine.com/business/sebi-fo-loss-study-explained-why-9-in-10-retail-traders-lost-91685-crore-in-fy26))
- [POST] After the Jane Street order (July 2025):
  - NSE index-option premium turnover on expiry fell from ₹80,731 crore (June 26) to ₹61,511 crore (July 3) to ₹45,884 crore (July 10).
  - Reuters reported about a 36% two-week drop to ₹39,626 crore on the July 17 expiry.
  - Total NSE turnover on the first Nifty expiry after the ban was down 21%.
  - Prop firms are about 60% of derivatives turnover. — [Millennium Post](https://www.millenniumpost.in/business/jane-street-scandal-slashes-nse-options-premium-turnover-by-35-619369); [Reuters via TradingView](https://tr.tradingview.com/news/reuters.com%2C2025%3Anewsml_L4N3TF08H%3A0-india-stock-exchange-derivative-activity-slips-by-a-third-since-jane-street-trading-ban); [Business Standard](https://www.business-standard.com/amp/markets/news/fo-turnover-dips-21-expiry-day-jane-street-ban-125071001169_1.html)

**Outcome data: individuals**
- [SPAN] SEBI's FY25 study (July 2025):
  - Individual net losses (after costs) rose about 41% to about ₹1.06 lakh crore, from ₹74,812 crore in FY24, and about 91% lost.
  - Unique individual traders fell from 61.4 lakh in Q1 FY25 to 42.7 lakh in Q4.
  - Losses rose through the first three quarters and eased in Q4, the first full post-change quarter. — [Business Standard](https://www.business-standard.com/markets/news/net-losses-of-traders-in-fo-widens-in-fy25-sebi-study-125070701221_1.html)
- [POST] SEBI's FY26 study (Aug 20, 2026). Figures for individual traders:

| Measure | FY25 | FY26 |
|---|---|---|
| Net losses | ~₹1.12 lakh crore (restated; see note) | ₹91,685 crore |
| Gross losses | ₹97,882 crore | ₹72,243 crore (−26%) |
| Share with net losses | 90.9% | 87.7% |

  - Note: the July 2025 study gave ₹1.06 lakh crore for FY25 net losses, so the FY25 figure appears restated or computed on a different basis.
  - Average loss per trader rose slightly, to about ₹1.17 lakh.
  - Active traders fell about 20%. The reported bases conflict: 98.1 → 78.6 lakh, or 106.2 → 87.5 lakh.
  - Cumulative FY22–FY26 net losses were about ₹3.85 lakh crore.
  - 57% of FY25 traders continued trading in FY26. — [Tribune](https://www.tribuneindia.com/news/business/nearly-9-in-10-individual-derivatives-traders-lost-money-in-fy26-losses-hit-rs-91685-crore-despite-fall-in-participation-sebi/); [BusinessToday](https://www.businesstoday.in/markets/story/proprietary-traders-derivatives-profits-fall-in-fy26-says-sebi-study-550558-2026-08-21); [TaxGuru](https://taxguru.in/sebi/sebi-studies-key-trends-retail-participation-trading-behaviour-profitability-equity-derivatives.html); [SEBI trading-behaviour study PDF](https://www.sebi.gov.in/sebi_data/attachdocs/aug-2026/1787233601328.pdf)
- [POST] FY26 transaction costs for individuals were about ₹25,000 crore, and about ₹1 lakh crore cumulatively over FY22–FY26. Note that ₹91,685 crore net minus ₹72,243 crore gross is only about ₹19,400 crore, so the cost figure does not reconcile; verify in the PDF — [CorpLawUpdates](https://www.corplawupdates.in/updates/sebi-equity-derivatives-retail-trader-study-fy26)

**Outcome data: prop traders and FPIs**
- [POST] Prop traders' gross derivatives profits fell 3% to ₹44,483 crore in FY26, from ₹45,955 crore in FY25, with about 98% of that from options.
- [POST] FPI gross profits fell 55% to ₹13,896 crore.
- [POST] About 99% of FPI and prop gross profits came from "algo entities", meaning entities that placed at least one algo order. — [BusinessToday](https://www.businesstoday.in/markets/story/proprietary-traders-derivatives-profits-fall-in-fy26-says-sebi-study-550558-2026-08-21)

**Capital requirements (practitioner)**
- [POST] Margin for a 0DTE Nifty short straddle (one lot) is about ₹3–3.25 lakh — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/position-sizing-part-3-sizing-option)
- [POST] Zerodha's ORB test used about ₹1.5 lakh margin per lot for selling-side positions — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/how-to-trade-opening-range-breakout)

### Inferences
- The changes reduced how many people trade and how many contracts they trade far more than they reduced money at risk.
  - Premium turnover fell only about 9–15%, while notional value and contract counts fell 30–40%.
  - The share of individuals losing barely moved: 91% in FY25 and 87.7% in FY26.
  - The fall in FY26 losses partly reflects about 20% fewer traders and a calmer market. The data do not isolate the effect of the rules.
- For premium sellers:
  - The removal of Bank Nifty, Fin Nifty and Midcap weeklies cut the number of weekly expiry days per exchange to one, which removes the "sell every day's expiry" approach.
  - The 2% ELM on expiry day and the loss of the calendar-spread offset raise expiry-day margin, which lowers return on margin for 0DTE selling.
  - A worked example of the ELM alone: 2% × strike 25,000 × 65 units ≈ ₹32,500 per short lot. This is my arithmetic, not a sourced figure.
- The Sept 2025 Tuesday/Thursday swap means 0DTE sellers now have two expiry days a week, Nifty on Tuesday and Sensex on Thursday. Sensex's role as a second 0DTE vehicle grew. Zerodha's Sensex 0DTE study is an example of practitioners moving there.
- Prop-firm profits held up (−3%) while FPI profits halved. That is consistent with the Jane Street order's effect being concentrated in FPIs, but the data do not prove it.

### Gaps
- I found no SEBI or exchange study isolating returns to premium-selling strategies, or to option buyers vs sellers, before vs after Nov 2024.
- Pre-Nov-2024 lot sizes (Nifty 25, Bank Nifty 15, Fin Nifty 25) and the April 2025 Bank Nifty/Nifty revisions are widely known but were not directly confirmed by sources retrieved this session. One source states Bank Nifty went from 25 to 35, which looks inconsistent and is unverified.
- I could not confirm whether SEBI formally adopted any 2026 change to weekly expiries or expiry-day settlement pricing.
- The FY25 net-loss revision (₹1.06 vs ₹1.12 lakh crore), the active-trader counts and the transaction-cost figure all conflict across secondary sources. The SEBI PDFs could not be fetched to resolve them.

---

## 4. What public backtest platforms (AlgoTest, Stockmock, Opstra, Sensibull, Tradetron, Quantman) show for 2020–2026, and evidence of survivorship bias and overfitting in marketplace strategies

### Takeaway
Platforms mostly provide tools and templates rather than published, dated performance studies. The few public prebuilt results, from QuantsApp for Oct 2025–Sep 2026, show most popular Nifty selling and buying templates negative after costs. I found no systematic independent study of Indian strategy-marketplace survivorship. Platforms themselves acknowledge overfitting risk, and SEBI's 2025 algo framework restricts the old open-marketplace model.

### Cited Findings
- AlgoTest's documentation uses a 9:20 straddle with a 25% stop-loss as its standard backtest tutorial template. Its blog provides frameworks and checklists (drawdown, losing streaks, concentration, costs) but no dated post-2024 performance results — [AlgoTest docs](https://docs.algotest.in/Time-Based-Algo-Trading/how-to-backtest/backtest-920-Straddle/); [AlgoTest short straddle blog](https://algotest.in/blog/short-straddle-strategy/)
- [POST] QuantsApp's public prebuilt backtests for Oct 2025–Sep 2026 were negative after costs for: the 9:20 strangle, the 9:20 straddle with stop-and-reverse (−₹1,09,914 after costs), the overnight straddle (+₹24,344 gross becomes −₹3,372 net), the 45-DTE straddle (profit factor 0.81) and hero-zero buying (profit factor 0.51). Figures are detailed in Q1 and Q2 — [QuantsApp](https://www.quantsapp.com/backtesting/strategies/overnight-short-options-close-to-open); [QuantsApp](https://www.quantsapp.com/backtesting/strategies/expiry-day-hero-zero-otm-buy)
- [SPAN] Zerodha's "In The Money" newsletter publishes post-cost backtests (ORB, 9:20 straddle, Sensex 0DTE, 45 DTE). These are among the more transparent practitioner sources because they state costs and slippage. Zerodha is a broker that earns from trading activity, though its content is often cautionary — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/we-backtested-the-famous-45-dte-strategy)
- Tradetron describes its marketplace as algorithms "run live in their creators' own accounts". Its own blog warns: "picking the best of 50 on one year of data can show an excellent Sharpe ratio, yet the same strategy on the next year returns to nothing." It offers holdout sweeps (optimize on an earlier period, validate on a later one) and advises comparing live trades with the backtest over the same dates — [Tradetron](https://tradetron.tech/); [Tradetron blog](https://tradetron.tech/blog/why-did-my-algo-strategy-fail-common-mistakes-and-fixes); [Tradetron blog](https://tradetron.tech/blog/what-to-do-when-your-live-algo-trades-dont-perform-as-expected)
- A third-party Indian F&O backtesting guide flags two pitfalls. One is survivorship bias in stock-option tests run on today's F&O list. The other is overfitting, which it suggests checking for a "plateau" of nearby parameter settings that also work — [FnOTrader](https://www.fnotrader.com/blog/options-backtesting-india)
- Under SEBI's Feb 2025 retail algo framework, individuals may share strategies only with family members. Platforms may offer their own strategies only with a Research Analyst licence and exchange registration, and changing a black-box algo's logic requires re-registering it as a new algo — [Zerodha Z-Connect](https://zerodha.com/z-connect/business-updates/explaining-the-latest-sebi-algo-trading-regulations); [MediaNama](https://www.medianama.com/2025/02/223-sebi-proposes-framework-retail-investors-algo-trading/)
- AlgoTradersLab's marketing shows sample P&L for 2024–2025 that cannot be verified — [AlgoTradersLab](https://www.algotraderslab.com/)
- An individual's "optimized" 9:20 straddle claims more than 80% annual returns on AlgoTest. This is a typical optimized-backtest claim without out-of-sample validation — [Medium](https://medium.com/@amit179.iitk2/optimized-920-straddle-strategy-to-get-more-than-80-return-annually-e977453dca80)

### Inferences
- Platform-published results are heavily template-driven and rarely show multi-year, dated, post-cost performance. Most strong numbers in circulation are user-optimized backtests, which carry a high risk of overfitting and selection.
- Marketplaces that show live P&L only for strategies still listed have a built-in survivorship problem: failed strategies drop out of view. Tradetron's own guidance acknowledges the in-sample-selection problem, but I found no data on delisted strategies.
- SEBI's RA-registration requirement for black-box providers, and the ban on sharing strategies outside family, should shrink the anonymous-creator marketplace model from 2026. The effect on quality is not yet measurable.
- Broker and platform vendors (QuantsApp, AlgoTest, Tradetron, Zerodha) earn from activity. Even so, the recent prebuilt results that are negative after costs run against their commercial interest, which makes them somewhat more credible.

### Gaps
- I found no published performance data from Stockmock, Opstra, Sensibull or Quantman for 2020–2026, and no independent audit of Tradetron marketplace live P&L, delisting rates or creator churn.
- I found no academic or regulatory study of survivorship bias in Indian algo strategy marketplaces.
- QuantsApp pages could not be fetched in full (network block), so drawdowns and trade counts for some templates are snippet-level only.

---

## 5. The July 2025 SEBI interim order against Jane Street: what it reveals about who is on the other side of retail options trades

### Takeaway
SEBI alleged that four Jane Street entities made more than ₹36,500 crore from Indian index derivatives over Jan 2023–Mar 2025. The alleged method was moving Bank Nifty constituents and futures intraday while holding much larger options positions. Combined with SEBI's studies, the case shows that algorithmic prop and FPI firms capture almost all derivatives profits while individuals are the only large loss-making group. The order itself is an allegation under appeal, and no source quantifies retail losses to Jane Street specifically.

### Cited Findings
- SEBI's interim order is dated July 3, 2025 and runs to 105 pages. It alleges four Jane Street entities made more than ₹36,500 crore from index derivatives between Jan 1, 2023 and Mar 31, 2025. SEBI impounded about ₹4,843 crore (some sources say ₹4,844 crore) and barred the entities from Indian markets — [CNBC](https://www.cnbc.com/2025/07/04/indian-regulator-bars-us-trading-firm-jane-street-from-accessing-securities-market.html); [Business Standard](https://www.business-standard.com/amp/markets/news/sebi-bars-jane-street-orders-rs-4844-cr-disgorgement-market-manipulation-125070400081_1.html); [Zee Business](https://www.zeebiz.com/market-news/news-sebi-vs-jane-street-inside-the-rs-36500-crore-derivatives-manipulation-that-rocked-d-street-372162)
- The alleged pattern was to buy Bank Nifty constituent stocks and futures in the morning to lift the index while holding large bearish index-option positions, then sell the same securities later in the day to depress the index. SEBI flagged 18 expiry days. It reportedly held that trades not themselves illegal became manipulative because of their scale and reversal without economic rationale — [Oxford Business Law Blog](https://blogs.law.ox.ac.uk/oblb/blog-post/2025/07/jane-street-and-expiry-day-trap-unpacking-sebis-crackdown-algorithmic); [CNBC](https://www.cnbc.com/2025/07/04/indian-regulator-bars-us-trading-firm-jane-street-from-accessing-securities-market.html); [Mondaq](https://www.mondaq.com/india/commoditiesderivativesstock-exchanges/1648134/sebis-interim-order-against-jane-street-allegations-of-index-manipulation-explained)
- One analysis breaks down the total as about ₹43,289 crore of options profit against about ₹7,687 crore of cash and futures losses. This comes from a Medium post and is less authoritative — [Medium (Parth Malpani)](https://parthmalpani.medium.com/jane-street-india-market-manipulation-case-analysis-c8e39ea1bc34)
- A July 21, 2025 modification order lifted the trading ban but added conditions on trading strategies. In October 2026, SEBI told the Securities Appellate Tribunal that Jane Street has enough data to respond and that the interim order could be vacated if Jane Street shows its trading was not manipulative. Jane Street disputes the findings — [Arekay Substack](https://arekay.substack.com/p/if-you-have-to-move-the-market-to); [BusinessToday (Oct 6, 2026)](https://www.businesstoday.in/markets/story/sebi-tells-sat-that-jane-street-has-enough-data-to-respond-to-market-manipulation-charges-559953-2026-10-06); [NewsBytes](https://www.newsbytesapp.com/news/business/sat-reserves-order-in-jane-street-document-disclosure-case/story)
- Jane Street netted about $2.3bn from Indian equity options trading (May 2025 report, before the order) — [Business Standard](https://www.business-standard.com/amp/markets/news/jane-street-nets-2-3-bn-from-booming-india-equity-options-trading-125052301072_1.html)
- Coverage says the alleged manipulation hurt participants on the other side, including retail traders. Experts note that retail losses specifically attributable to Jane Street's trades have not been quantified — [Business Standard](https://www.business-standard.com/amp/markets/news/jane-street-sebi-derivatives-retail-warning-manipulation-order-125070401079_1.html); [Al Jazeera](https://www.aljazeera.com/economy/2025/7/18/indias-ban-on-jane-street-raises-concerns-over-regulator-role)
- Context from SEBI studies on who wins:
  - [PRE] FY22–FY24: about 97% of FPI profits and 96% of prop-trader profits came from algo entities. — [MadeForTrade summary](https://madefortrade.in/t/sebi-study-91-of-traders-are-losing-money-in-f-o-proprietary-firms-cash-in/32122); [Navia](https://navia.co.in/blog/who-made-the-money-in-options-trading/)
  - [POST] FY26: about 99% of FPI and prop gross profits came from algo entities, and prop profits were about 98% from options. Individuals were the only major category with an aggregate loss. — [BusinessToday](https://www.businesstoday.in/markets/story/proprietary-traders-derivatives-profits-fall-in-fy26-says-sebi-study-550558-2026-08-21); [Tribune](https://www.tribuneindia.com/news/business/nearly-9-in-10-individual-derivatives-traders-lost-money-in-fy26-losses-hit-rs-91685-crore-despite-fall-in-participation-sebi/)
- Prop trading firms account for about 60% of derivatives turnover. After the ban, NSE expiry premium turnover fell by about a third in two weeks — [Business Standard](https://www.business-standard.com/amp/markets/news/fo-turnover-dips-21-expiry-day-jane-street-ban-125071001169_1.html); [Reuters via TradingView](https://tr.tradingview.com/news/reuters.com%2C2025%3Anewsml_L4N3TF08H%3A0-india-stock-exchange-derivative-activity-slips-by-a-third-since-jane-street-trading-ban)
- Retail made up 42% of 0DTE volume by the end of the Animal Spirits sample — [CFR Cologne WP](https://www.cfr-cologne.de/download/workingpaper/cfr-25-09.pdf)
- SEBI's intraday position-limit framework (₹5,000 crore intraday net, with snapshots including 2:45–3:30 pm) came after the Jane Street case — [Business Standard](https://www.business-standard.com/amp/markets/news/sebi-stricter-intraday-position-limits-options-market-regulation-125090200971_1.html)

### Inferences
- The counterparty to retail option flow is mostly sophisticated, algorithmic prop and FPI liquidity providers. Their profits are about 96–99% concentrated in algo entities and about 98% options-driven, while individuals lose in aggregate every year. The SEBI data support this at aggregate level, but no source maps trade-by-trade counterparties.
- The Jane Street allegations show a specific risk for expiry-day retail strategies, both 0DTE buyers and 9:20 straddle sellers with tight stops. A participant with enough capital can move the underlying intraday, so "technical" breakouts or stop triggers near expiry may be manufactured rather than informational. This is an allegation-based inference; the case is unresolved.
- The roughly one-third drop in expiry premium turnover after the ban shows how dependent the expiry-day market is on a handful of large prop/HFT firms. Thinner books mean wider spreads and more slippage for retail algos, which compounds the cost drag seen in post-cost backtests.

### Gaps
- No source quantifies retail losses on the 18 flagged expiry days or identifies retail's share of Jane Street's counterparties. The SEBI order itself (sebi.gov.in) could not be fetched.
- The final outcome of the Jane Street case (SAT / final order) was not found as of Oct 2026.

---

## 6. Minimum practical capital for hedged option selling (iron condor / iron fly) on Nifty after the lot-size changes

### Takeaway
At the current Nifty lot of 65 (from Jan 2026), broker-blocked margin for a one-lot hedged iron condor or fly is typically quoted at roughly ₹40,000–₹80,000. Estimates range from about ₹15,000 to ₹2 lakh depending on wing width, volatility, broker and expiry-day ELM. A naked 0DTE straddle needs about ₹3–3.25 lakh. "Practical" capital, meaning enough to absorb drawdowns and stagger entries, is a multiple of the margin.

### Cited Findings
- [POST] The Nifty lot is 65 (was 75) from the Jan 6, 2026 weekly and Jan 27, 2026 monthly contracts — [5paisa](https://www.5paisa.com/blog/index-derivatives-new-lot-sizes-nse-update-january-2026)
- The minimum contract value for index derivatives is ₹15 lakh at introduction, with lots kept in a ₹15–20 lakh band — [Business Standard](https://www.business-standard.com/amp/markets/news/sebi-announces-six-key-changes-to-curb-speculation-in-derivatives-trading-124100101316_1.html)
- Zerodha Varsity cites broker margin of about ₹44,303 for a Nifty iron condor vs about ₹1.45 lakh for a short strangle. The lot size and date of that example are unclear, and it may predate the 2024 changes — [Zerodha Varsity](https://zerodha.com/varsity/chapter/iron-condor/) (as summarized in search)
- Broker and education blogs give other figures. All are 2026-dated broker or educator content, not exchange SPAN documents:
  - About ₹40,000–60,000 per lot for 200-point wings. — [GoPocket](https://www.gopocket.in/blog/iron-condor-strategy-india-nifty-secrets-2026)
  - About ₹15,000–25,000 per lot after hedge credit (another source). — [PaperPe](https://paperpe.in/blog/iron-condor-strategy-india)
  - ₹80,000–2,00,000 per lot depending on volatility, width, expiry and broker. — [NiftyTrader](https://www.niftytrader.in/markets/iron-condor-strategy-when-to-use-avoid/)
  - One worked example: formula-based max-risk margin of ₹6,559, while the broker blocked ₹68,039 (SPAN plus exposure). — [Strike.money](https://www.strike.money/options/iron-condor)
- Exchanges recognize the long wings as hedges, so a condor needs far less margin than four naked legs — [Flattrade](https://flattrade.in/learn/glossary/iron-condor/)
- [POST] For comparison, a naked 0DTE Nifty short straddle needs about ₹3–3.25 lakh margin per lot (Feb 2026) — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/position-sizing-part-3-sizing-option)
- [POST] On expiry day, an extra 2% ELM on contract value applies to short options, and calendar-spread offsets are removed for contracts expiring that day — [Arihant Capital](https://blog.arihantcapital.com/sebi-tightens-the-reins-introduces-6-new-measures-for-fo-trading/)
- [POST] Upfront premium collection (from Feb 1, 2025) means hedge legs must be fully paid at entry — [Arihant Capital](https://blog.arihantcapital.com/sebi-tightens-the-reins-introduces-6-new-measures-for-fo-trading/)
- [POST] The Sensex 0DTE study shows that splitting six lots into six staggered entries raised return/max-drawdown from 0.64 to 2.56. Diversifying entries requires enough capital for several lots — [In The Money by Zerodha](https://inthemoneybyzerodha.substack.com/p/sensex-0dte-straddle-or-strangle)

### Inferences
These are my own arithmetic, not sourced figures.
- **Maximum loss.** An iron condor or fly with 200-point wings on one 65-unit lot has a maximum gross loss of about 200 × 65 = ₹13,000 on one side, less the credit received. Broker margin exceeds this because of SPAN and exposure add-ons and the expiry-day ELM.
- **Expiry-day ELM.** At a Nifty strike of about 25,000, 2% ELM ≈ ₹32,500 per short lot, which could dominate margin on 0DTE iron flies.
- **Single-lot capital.** About ₹50,000–₹1 lakh per lot is a reasonable planning range for margin, consistent with the sourced ₹40,000–80,000 typical range plus buffer.
- **Diversified capital.** Given drawdown evidence (QuantsApp 9:20 strangle max drawdown about ₹36,000 per lot-equivalent in Oct 2025–Sep 2026) and the benefit of staggered entries, practitioners would likely need ₹2–5 lakh to run hedged selling across several entries or lots without one bad day dominating.
- **Effect of the lot cut.** It reduced per-lot capital by about 13% (65/75) versus 2025. Per-lot capital remains about 2.5–3× its pre-Nov-2024 level, assuming the widely reported pre-change Nifty lot of 25, which was not directly verified here.

### Gaps
- I found no exchange (NSE SPAN) or broker-calculator snapshot dated 2026 for a specific Nifty iron condor or fly at lot 65 with stated strikes and wings. All margin figures are from blogs and education pages.
- I found no source quantifying typical annual return on margin for retail iron condors or flies on Nifty after Nov 2024.
- The Varsity ₹44,303 / ₹1.45 lakh example could not be dated or tied to a lot size.
