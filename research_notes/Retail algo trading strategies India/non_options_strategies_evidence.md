# Evidence on Non-Options Systematic Trading Strategies in Indian Markets (for a Retail Kite Connect Algo Trader)

*Current as of 2026-10-29. Evidence labels used throughout: **[LIVE]** = real fund/PMS/index-fund track record; **[INDEX-BACKCALC]** = NSE index history computed before the index's launch date (a backtest); **[BACKTEST]** = blog/vendor/practitioner simulation; **[ACADEMIC]** = peer-reviewed or working-paper study (usually gross of costs and often long-short); **[PROMO]** = fund-house marketing figure. Method note: direct fetches of niftyindices.com, wrightresearch.in and jrvarma.in were blocked by this session's network settings, so NSE factsheet figures below come from search-engine extracts, fund-house documents and aggregators. Check them against primary factsheets before relying on them.*

**Market backdrop for "the weak-index period" (late 2024 to 2026), used across sections:**
- Nifty 50 was down about 14% from its peak by March 2025 (Motilal Oswal view) — [Business Standard](https://www.business-standard.com/amp/markets/news/indian-equities-may-be-nearing-correction-bottom-says-motilal-oswal-125031201051_1.html). The fall from October 2024 was the Nifty's biggest in 10 years — [Business Standard, Jan 2025](https://www.business-standard.com/amp/markets/news/nifty-fall-since-october-2nd-biggest-in-10-years-16-stocks-tank-over-20-125012800225_1.html)
- CY2025: Nifty 50 was up about 10.71% YTD as of 23 Dec 2025 (about 23,644 to 26,172) — [Angel One](https://oga-prod.angelone.in/news/economy/gold-vs-nifty-performance-2025-recap-how-precious-metals-compared-with-equities). Nifty 500 was up about 7% for 2025 — [5paisa citing 1 Finance](https://www.5paisa.com/index.php/news/gold-rallied-72-and-silver-122-in-2025-while-nifty-500-rose-7). The Nifty set no new record high in 2025 (it set 65 in 2024) — [Business Standard, Oct 2025](https://www.business-standard.com/amp/markets/news/nifty-misses-new-highs-this-cy-after-record-2024-gold-takes-the-spotlight-125101300069_1.html). The Nifty Smallcap 250 fell 6.0% in CY25 after +48.1% (CY23) and +26.4% (CY24) — [Ambit newsletter Aug 2026](https://www.ambit.co/newsletter/newsletter-august-2026/)
- CY2026: Nifty 50 was down 14.4% and Sensex down 15.6% YTD (article dated 13 Oct 2026). Net FPI selling was about ₹3.08 trn YTD versus ₹1.66 trn in all of 2025, and DIIs bought about ₹6.83 trn — [Angel One](https://www.angelone.in/news/economy/fpi-selling-reaches-3-08-trillion-in-cy26-as-october-2026-outflows-cross-47-000-crore). (Single source for the -14.4% figure. Treat it as approximate.)

---

## 1. Momentum / factor strategies: academic evidence and NSE factor indices (Nifty200 Momentum 30, Nifty500 Momentum 50, Nifty Alpha 50, Low Volatility 30, Quality 30)

### Takeaway
Academic and index evidence shows a strong long-run momentum premium in India (the IIMA momentum factor averaged about 21.9% a year gross, long-short, 1994–2013). NSE momentum indices show roughly 4–5 percentage points of annual CAGR over the Nifty 200, but most of that history is back-calculated. The first truly live stress test went badly: Nifty200 Momentum 30 fell about 30–32% from September 2024 to March/April 2025, had roughly zero 1-year returns through August 2026, and index funds tracking it still had not regained their 2024 peaks as of August 2026. Low-volatility and quality tilts show smaller drawdowns in down years, but full 2025–2026 index numbers could not be verified.

### Cited Findings
**Academic evidence [ACADEMIC]**
- Agarwalla, Jacob and Varma (IIM Ahmedabad WP 2013-09-05, revised Sep 2014) built India Fama-French and momentum factors from CMIE Prowess data for Oct 1993–Dec 2013. They excluded illiquid stocks so the portfolios are investable and corrected for survivorship bias. Momentum (WML) had the highest average annual return, 21.9%, against a market risk premium of 11.5%. The factor series is kept in a monthly-updated IIMA data library — [IIMA publication page](https://www.iima.ac.in/publication/four-factor-model-indian-equities-market); [working paper PDF](https://web.iima.ac.in/~iffm/legacy/four-factors-India-90s-onwards-IIM-WP-Version-original-Sep13.pdf); [data library](https://www.jrvarma.in/fama-french.html). (The abstract's date range contains an apparent typo. Some figures in the extracted text were garbled.)
- Ansari & Khan (2012) found strong momentum profits in India over 1995–2006 that CAPM and Fama-French models fail to explain — [Emerald, "Momentum anomaly: evidence from India"](https://emerald.com/insight/content/doi/10.1108/03074351211193730/full/html)
- Maheshwari & Dhankar (2017) used 470 BSE stocks from Jan 1997 to Mar 2013 and found that some aspects of the momentum effect differ from those reported for the USA — [IDEAS/RePEc](https://ideas.repec.org/a/eme/jamrpp/jamr-11-2015-0081.html)
- Bernard & Deo studied BSE-500 constituents from Jul 2004 to Jun 2014 and report economically and statistically significant momentum profits — [publishingindia PDF](https://publishingindia.com/storage/PDFBrochures/3029.pdf) (attribution of this exact URL to that paper comes from a search summary and is not verified)
- Quantpedia's "Performance of Factor Strategies in India" covers long-short factor portfolios from Apr 1995 to Mar 2021. Average drawdown is 12.13% for momentum versus 9.76% for the QMJ quality factor, and 14.52% versus 7.99% in the "LQ" variant — [Quantpedia](https://quantpedia.com/performance-of-factor-strategies-in-india/)
- Quantpedia lists a "Long Term Time-series Momentum in India" strategy, 2010–2019 backtest: indicative return 16.02%, volatility 15.1% [BACKTEST] — [Quantpedia update, May 2021](https://vvv.quantpedia.com/?p=12773)
- A practitioner commentary on rolling 5-year windows versus the Nifty 200 says momentum beat the index in 99% of observations with average alpha of 6%, low volatility in 96% and quality in 87%. It names quality as the best factor in FY2025 [INDEX-BACKCALC mostly] — [Momentum Lab substack](https://momentumlab.substack.com/p/factor-this-october-2024) / [Freefloat substack](https://freefloat.substack.com/p/factors-buy-all-of-them) (the search summary did not say which of these two pages holds the numbers)

**Nifty200 Momentum 30**
- NSE launched it on 25 Aug 2020 with base date 1 Apr 2005, so the history before Aug 2020 is back-calculated. It selects the top 30 Nifty 200 stocks on volatility-adjusted 6- and 12-month price returns and rebalances semi-annually in June and December — [NSE press release](https://niftyindices.com/Press_Release/ind_prs25082020.pdf); [NSE whitepaper](https://www.niftyindices.com/docs/default-source/indices/nifty200-momentum-30/nifty200_momentum_30_index_whitepaper_sep_20.pdf)
- TRI CAGR from 1 Apr 2005 to 30 Jun 2026 was 18.8%, versus 13.9% for the Nifty 200 TRI [INDEX-BACKCALC + live since 2020]. The Sep 2025 leaflet showed 19.3% versus 14.3% — [HDFC MF PPT, July 2026](https://files.hdfcfund.com/s3fs-public/Others/2026-07/HDFC%20NIFTY200%20Momentum%2030%20Index%20Fund_PPT%20%28July%202026%29.pdf); [HDFC leaflet, Sep 2025](https://files.hdfcfund.com/s3fs-public/Others/2025-10/HDFC%20NIFTY200%20Momentum%2030%20Index%20Fund%20%20Leaflet%20September%202025.pdf). (The June 2026 HDFC leaflet labels 18.8% versus 13.9% as a "10-year CAGR" as of 29 May 2026. The labels conflict — [HDFC leaflet June 2026](https://files.hdfcfund.com/s3fs-public/Others/2026-06/Leaflet%20-HDFC%20NIFTY200%20Momentum%2030%20Index%20Fund%20%28June%202026%29.pdf))
- Index drawdown was about -31.79%, from 27 Sep 2024 to 7 Apr 2025. That is the second-deepest since 2010, after the COVID crash at about -34.2%. The source blames rapid sector rotation (defensives, then banks and capital goods, then mid/small caps) and macro/geopolitical shocks. It also reported a 5-year return of 154% as of March 2025 — [Curious Investing Insights substack](https://curiousinvestinginsights.substack.com/p/momentum-or-mayhem-unpacking-the)
- [LIVE] The Kotak Nifty 200 Momentum 30 Index Fund had a max drawdown of -30.13% (27 Sep 2024 to 14 Mar 2025) and a 1Y return of 0.66% versus a category average of 7.24%. Its worst rolling 1-year window was about -15% to -21%, ending around Sep/Oct 2025, and it had not regained its prior peak as of its Aug 2026 update — [arthgyaan Kotak](https://arthgyaan.com/fund/kotak-nifty-200-momentum-30-index-fund-direct-growth/151781). The Motilal Oswal fund returned 0.53% over 1Y versus a category average of 7.29% (as of 21 Aug 2026) and ranked 154/185 in 2025 — [arthgyaan Motilal](https://arthgyaan.com/fund/motilal-oswal-nifty-200-momentum-30-index-fund-direct-growth/149800)
- [LIVE] The index fell 1.59% in July 2026. Its trailing 12-month average monthly price return (Aug 2025–Jul 2026) was about -0.22% — [Wright Research](https://www.wrightresearch.in/blog/how-did-the-nifty200-momentum-30-perform-in-july-2026/)
- Older analysis: average 5-year rolling returns (rolled daily over the prior 15 years) were 28.4% for the Nifty momentum index (undated, mostly back-calculated) — [PrimeInvestor](https://primeinvestor.in/?p=43951)

**Nifty500 Momentum 50**
- NSE announced it in June 2024: the top 50 momentum stocks from the Nifty 500, chosen on volatility-adjusted 6- and 12-month returns, rebalanced semi-annually, base date 1 Apr 2005 — [Business Standard](https://www.business-standard.com/amp/markets/capital-market-news/nse-launches-new-index-targeting-high-momentum-stocks-in-nifty-500-124060600490_1.html)
- [PROMO/INDEX-BACKCALC] Motilal Oswal marketing quoted a 25.2% CAGR since Apr 2005 versus 15.2% for the Nifty 50, using NSE data to 31 Jul 2024. The index launched about a month before the 2024 peak — [TradingQnA thread](https://tradingqna.com/t/motilal-oswal-nifty-500-momentum-50-index-fund/172852)
- Business Standard (Nov 2024) warned that "high returns in back tests might not always persist" once a fund launches, and said index choice should depend on behaviour in downturns — [Business Standard](https://www.business-standard.com/finance/personal-finance/choice-of-momentum-factor-index-should-depend-on-performance-in-downturns-124110701113_1.html)
- No reliable index-level drawdown or 2025–2026 return was found. Aggregator figures (for example, a -0.32% "max drawdown" on Sharpely) are implausible.

**Nifty Alpha 50**
- In the 2020 COVID crash the index fell 38.3% in about 32 days, versus 31% for the Nifty100 Low Volatility 30 — [Groww Digest](https://digest.groww.in/p/what-if-we-compare-the-calmest-stocks)
- As of 18 Jul 2025 it was down 11.08% year on year — [HDFC Sky](https://hdfcsky.com/news/nifty-alpha-50-sinks-1-01-percent-as-92-percent-stocks-decline)

**Low volatility**
- The Nifty100 Low Volatility 30 holds the 30 least-volatile Nifty 100 stocks, weighted by inverse volatility and rebalanced quarterly. In 2008 it still fell -49.5% (2 Jan to 27 Oct 2008) — [NSE white paper, Jun 2018](https://archives.nseindia.com/content/indices/NIFTY100_Low_Vol30_White_paper_Jun2018.pdf)
- Its annualised volatility is about 14%, versus 16.5% for the Nifty 50. It tends to lag in strong bull markets — [Business Standard, Apr 2025](https://www.business-standard.com/amp/finance/personal-finance/low-volatility-index-funds-etfs-show-lower-drawdowns-and-higher-returns-125040300960_1.html)
- Issuer calculation: in Nifty 100 up-years the index averaged 29.7% versus 29.3% for the Nifty 100. In down-years it averaged -5.5% versus -13.6% — [HDFC Low Vol 30 leaflet, July 2026](https://files.hdfcfund.com/s3fs-public/Others/2026-08/HDFC%20Nifty100%20Low%20Volatility%2030%20Index%20Fund%20-%20Leaflet%20%28as%20on%20July%202026%29.pdf)
- [LIVE] The ICICI Pru Nifty 100 Low Vol 30 ETF had a 2020 max drawdown of about -26% (Jan to early Apr 2020) and recovered by 21 Aug 2020 — [arthgyaan](https://arthgyaan.com/fund/icici-prudential-nifty-100-low-volatility-30-etf/141596)
- Nifty Alpha Low-Volatility 30 had a 19.0% CAGR since 2005 inception, versus 13.2% for the Nifty 100 [INDEX-BACKCALC] — [NSE whitepaper 2020](https://www.niftyindices.com/docs/default-source/indices/nifty-alpha-low-volatility-30/nifty-alpha-low-volatility-30-whitepaper_2020.pdf)
- Blended factor indices in 2026: Nifty Quality Low-Volatility 30 1Y return was -4.36% (June 2026) or -7.38% (12 Jun 2026), with a 3Y return of 7.09% — [Anand Rathi](https://anandrathi.com/indices/nifty-quality-low-volatility-30); [5paisa](https://www.5paisa.com/share-market-today/nifty-quality-low-volatility-30). Nifty Alpha Quality Low-Vol 30 1Y was +1.20% with beta 0.86 (21 Jul 2026) — [IndexPE](https://www.indexpe.in/nifty-alpha-quality-low-volatility-30). Nifty Alpha Quality Value Low-Vol 30 1Y TR was -2.42% with beta 0.85 — [IndexPE](https://www.indexpe.in/nifty-alpha-quality-value-low-volatility-30)

**Quality**
- Nifty200 Quality 30 picks the top 30 Nifty 200 stocks on ROE, debt/equity and 5-year EPS-growth variability, rebalanced semi-annually (factsheet dated 30 Sep 2026). The return table could not be parsed reliably — [NSE factsheet](https://www.niftyindices.com/Factsheet/Factsheet_Nifty200_Quality30.pdf)

**Live practitioner momentum/quant**
- Capitalmind said the smallcase version of its momentum strategy "seemed stretched compared to realised returns for most investors" and began publishing an internal NAV. Model portfolios overstate what investors actually get — [Capitalmind momentum review, 2022](https://premium.capitalmind.in/2022/01/capitalmind-momentum-review/)
- [LIVE] Capitalmind Market PMS fell -15.48% (30 Oct 2024 to 28 Feb 2025) but returned 23.86% over 1Y versus 11.08% for the Nifty 50 TRI (to 31 May 2025). Capitalmind Resilient PMS fell -21.70% (29 Sep 2024 to 28 Feb 2025) — [zfunds Market](https://zfunds.in/portfolio-management-services/capitalmind-market); [zfunds Resilient](https://zfunds.in/portfolio-management-services/capitalmind-resilient)

### Inferences
- The momentum premium is well documented in Indian academic data. Its live retail form (a long-only top-30 or top-50 basket rebalanced semi-annually) captures only the long leg. It carries roughly market beta plus crash risk at regime turns, as Sep 2024–Mar 2025 showed.
- Momentum crowding rose sharply after 2020, with many momentum index funds launched in 2023–2024 near the peak. The weak live record since launch fits back-tests overstating realisable returns. Two years is too short to reject the premium, but a retail backtest should assume lower forward returns than the 18–25% back-calculated CAGRs.
- A Kite Connect replication of Nifty200 Momentum 30 needs about 30 cash-equity positions and twice-yearly rebalancing. Capital needs are modest (₹2–5 lakh lets weights be approximated), but delivery STT and STCG tax on each rebalance add drag that NSE TRI figures ignore. This estimate is not sourced.
- Low-volatility and quality tilts were the more defensive factor sleeves on the evidence available (down-year average -5.5% versus -13.6%). 2026 1Y returns for the blended low-vol indices were still around -7% to +1%, so they cut losses rather than avoiding them.

### Gaps
- Could not retrieve NSE factsheets directly (niftyindices.com blocked for fetch), so verified since-inception CAGR, max drawdown and calendar 2025/2026 returns for Nifty Alpha 50, Nifty200 Quality 30, Nifty100 Low Volatility 30 and Nifty500 Momentum 50 are missing. Pull the TRI history from niftyindices.com.
- No index-level 2008 drawdown figure for the momentum indices was found. Back-calculated 2008 drawdowns are reportedly much deeper than 2020 or 2024–25, but this was not verified.
- Recent academic momentum Sharpe ratios for India (for example a 2024 Nifty 500 study covering 2015–2024) were found, but no figures were extracted.
- Live momentum PMS returns for 2025–2026 (for example Capitalmind Momentum, Wright Momentum) were not found.

---

## 2. Trend following / time-series momentum on Nifty futures, stock futures and MCX commodities; gold/silver versus Nifty in 2024–2026

### Takeaway
India-specific evidence for trend following is thin and mixed. One 2014 study of 80 trend rules on the Nifty found they worked mainly in sharp declines and poorly in grinding or trendless markets. Academic MCX momentum studies find weak results after costs. Practitioner backtests (StockViz on Zerodha Varsity) find that combining Nifty and gold trend systems roughly halves drawdown, while crude oil was the main drag. 2025–2026 was a strong trending environment for precious metals and a weak one for the Nifty: gold +72% and silver +122% in 2025 versus Nifty 500 +7%. A gold trend-follower would have done far better than a Nifty one.

### Cited Findings
- [ACADEMIC] Slivka, Keswani and Li (2014) tested 80 trend-following algorithms on Nifty closing prices from 2005 to 2012. The rules worked well in a sharply declining market and much less well, or not at all, in gradually rising, mixed-trend or nearly trendless markets — [Indian Journal of Finance](https://www.indianjournalofentrepreneurship.com/index.php/IJF/article/view/71980)
- [ACADEMIC] Barik & Balakrishnan (2017) examined short- and long-term momentum in 16 MCX commodities from Nov 2005 to Oct 2016. They conclude commodity futures "are not an alternative investment class" because they fail to offer risk diversification — [JCRM, "Is Momentum Effect Present in Indian Commodity Market?"](https://jcrm.psgim.ac.in/index.php/jcrm/article/view/657)
- [ACADEMIC] An NITK study of 13 MCX contracts (Jun 2006–Apr 2016) tested momentum, term-structure and idiosyncratic-volatility strategies. After transaction costs and risk adjustment, idiosyncratic-volatility strategies were more profitable than momentum strategies — [NITK repository](https://idr.nitk.ac.in/items/043ffc9d-0415-4145-a897-f37e31f2d4d0)
- [BACKTEST] StockViz's "Could trend following be a successful trading strategy?" series on Zerodha Varsity — [Part II](https://zerodha.com/z-connect/varsity/could-trend-following-be-a-successful-trading-strategy-part-ii); [Part III](https://zerodha.com/z-connect/varsity/could-trend-following-be-a-successful-trading-strategy-part-iii):
  - Gold is more negatively correlated with the Nifty 50 than silver is.
  - An equal-weight Nifty 50 plus gold MA-crossover system had about a 10% validation-period drawdown versus about 20% for single-asset versions, with "mid-teens returns".
  - A four-asset MCX basket had a max drawdown of about 10%; with 2x leverage it reached "mid-20s" returns. Crude oil was "the biggest culprit" for underperformance.
  - "A flat market is kryptonite for trend-following strategies."
  - Costs were assumed at 25 bps of notional.
  - Part IV used a 5×N crossover with N from 50 to 500 to avoid data mining. It noted that dropping copper and crude with hindsight would "boost performance by several points", which illustrates selection bias.
- [BACKTEST] Quantpedia's long-term time-series momentum in India (2010–2019) showed about 16.0% return at 15.1% volatility — [Quantpedia](https://vvv.quantpedia.com/?p=12773)

**Gold/silver versus Nifty 2024–2026 [LIVE market data]**
- 2025: gold +72%, silver +122%, Nifty 500 +7%. Indian equities were also hit by FPI outflows and about 6% INR depreciation — [5paisa citing 1 Finance](https://www.5paisa.com/index.php/news/gold-rallied-72-and-silver-122-in-2025-while-nifty-500-rose-7). Nifty 50 was +10.71% YTD to 23 Dec 2025 versus gold about +70% — [Angel One](https://oga-prod.angelone.in/news/economy/gold-vs-nifty-performance-2025-recap-how-precious-metals-compared-with-equities). By mid-Oct 2025, Nifty/Sensex were up about 6.5% versus gold +58% and silver +80% — [Business Standard](https://www.business-standard.com/amp/markets/news/nifty-misses-new-highs-this-cy-after-record-2024-gold-takes-the-spotlight-125101300069_1.html)
- Conflicting figure: Nithin Kamath was cited as reporting gold +18% versus Nifty LargeMidcap 250 -6% in an early-April 2025 snapshot (a partial-year figure) — [Business Today](https://www.businesstoday.in/amp/personal-finance/investment/story/zerodhas-nithin-kamath-highlights-how-this-asset-had-superior-returns-over-stocks-since-2000-470824-2025-04-05)
- Silver ETFs: Tata Silver ETF 1Y return was 208.14% and ABSL Silver ETF 206.87% as of Jan 2026 (1-year, not YTD) — [Angel One](https://www.angelone.in/news/mutual-funds/top-10-etfs-with-over-200-percent-ytd-gains-as-of-jan-2026-tata-silver-etf-aditya-birla-sl-and-more)
- 2026: gold ETFs were up about 16% YTD by Akshaya Tritiya (April 2026) — [Angel One](https://www.angelone.in/news/commodities/akshay-tritiya-2026-gold-delivers-up-to-61-returns-since-last-year). On 21 Apr 2026 the Nifty/gold ratio was 1.62 (Nifty 24,576.60; gold 999 at ₹15,215.50/g), a 5-year low — [share.market](https://www.share.market/buzz/insights/the-nifty-to-gold-ratio-a-compass-for-investors-in-times-of-war-and-market-volatility/)
- MCX gold hit record highs in August 2026 (about ₹162,500/10g on 26 Aug) and then pulled back. On 30 Sep 2026, MCX gold was about ₹150,177/10g and silver about ₹226,650/kg. Gold was still up more than 28% over 1 year, and silver was up about 85% over 1 year (17 Sep) — [StartupTalky 26 Aug](https://startuptalky.com/news/gold-silver-prices-india-today-26-august-2026-both-ease-further/); [StartupTalky 17 Sep](https://startuptalky.com/news/gold-silver-prices-india-today-17-september-2026-both-metals-ease/); [StartupTalky 30 Sep](https://startuptalky.com/news/gold-silver-prices-india-today-30-september-2026/) (single aggregator; data internally inconsistent in places)

### Inferences
- With the Nifty down about 14% YTD in 2026 and gold up about 28% over 1 year to September, a simple trend filter (for example price above its 200-day average) would have kept a trader largely out of the Nifty and long gold/silver for most of 2025–2026. That matches the "trend works in declines and strong trends" finding. The August–September 2026 metals pullback (gold about -8% from its August high) is the kind of whipsaw that hurts.
- For Kite Connect, MCX gold/silver mini contracts and Nifty futures are the practical instruments. The SEBI ₹15–20 lakh index-futures contract size (see Q5) makes a diversified Nifty-futures trend system impractical below about ₹5–10 lakh of margin capital. Gold/silver ETFs (GOLDBEES and similar) allow small-ticket long-only trend following with no shorting.
- Crude oil and natural gas were drags in the StockViz backtests, and Indian commodity momentum studies are weak. Excluding assets after seeing results is data-snooping.

### Gaps
- No peer-reviewed study applying time-series momentum to Nifty futures or Indian stock futures specifically was found. Moskowitz-Ooi-Pedersen and AQR/Man trend papers were not confirmed to include Indian markets.
- Exact CAGR, Sharpe and max-drawdown numbers for the StockViz MCX backtests appear only in charts and were not extracted. The Zerodha "In The Money" MCX backtest results were not found.
- No clean, sourced YTD-2026 gold or silver return to late October 2026 was found. Jan 2026 spot-gold prints were inconsistent across sources (about $5,537/oz on 29 Jan versus about $4,841 on 3 Feb), so they are not used.

---

## 3. Mean reversion (short-term reversal, RSI(2)-type, Bollinger band) on Indian large caps/indices: evidence and decay

### Takeaway
Indian academic evidence supports reversal at very short (intraday) and longer (multi-month to multi-year) horizons, with momentum at 6–12 months in between. No published, credible RSI(2) or Bollinger-band backtest on the Nifty or Indian large caps was found, and nothing on decay. US/European RSI(2) results are vendor claims and do not carry over automatically.

### Cited Findings
- [ACADEMIC] Tripathi & Aggarwal used high-frequency data and found that Indian stock prices reverse within minutes of extreme rises and falls, with reversals after falls being quicker — [International Journal of Financial Management](https://publishingindia.com/archive/ijfm/prior-return-effect-in-indian-stock-market-an-intra-day-analysis)
- [ACADEMIC] Parthasarathy & Sendilvelu (2022) studied large, liquid Indian stocks. They found significant reversals for up to six months after both large monthly declines and large increases, and stronger initial shocks were followed by stronger reversals (overreaction) — [CEEOL](https://ceeol.com/search/article-detail?id=1054639)
- [ACADEMIC] Joshipura (NSE data, 1995–2008) found momentum profits over 6 and 12 months and contrarian returns over 3 years. Saji (2023, Nifty stocks 2008–2016) found losers outperform prior winners over 1–2-year formation periods — reported in a search summary; candidate sources [Inderscience "Mean reversals and stock market overreactions: further evidence from India"](https://inderscience.com/filter.php?aid=132959) and [publishingindia PDF](https://www.publishingindia.com/storage/PDFBrochures/2481.pdf) (exact URL-to-paper attribution not verified)
- [BACKTEST] The original Connors RSI(2) rules: long only above the 200-day SMA, enter when RSI(2) is below 10 (or below 5), exit on a close above the 5-day average. A vendor backtest reports +26.9% on the Nasdaq 100, +18.1% on the S&P 500 and +14.4% on the DAX (period unspecified), and failure on EUR/USD because that pair lacks upward drift — [Backtrex](https://backtrex.com/en/backtests/connors-rsi-2-eur-usd); [LuxAlgo RSI-2 concept](https://www.luxalgo.com/library/concept/rsi-2.md)
- [BACKTEST] StockCharts tested an RSI(5) cross-30/cross-70 system on the S&P 500. The best version reached a 9.52% compound annual return with a 21.49% max drawdown — [StockCharts, Arthur Hill](https://stockcharts.com/articles/arthurhill/2016/07/systemtrader---testing-a-basic-mean-reversion-system---catch-the-knife-or-wait-for-the-bounce-.html)

### Inferences
- RSI(2)-style index dip-buying depends on long-run upward drift plus short-term overreaction. The Nifty has historically had drift, but in a year like 2026 (about -14% YTD with persistent FPI selling) a filter of "price above 200-DMA" would have kept the system mostly flat. Without the filter it would have repeatedly bought falling markets.
- Short-horizon reversal on single stocks needs frequent trading. Indian round-trip costs (STT, exchange charges, stamp duty, GST, slippage) scale with turnover, so the intraday reversal edge documented by Tripathi & Aggarwal is unlikely to survive retail costs at the "minutes" horizon. This is untested inference.
- Overnight shorting of single stocks requires futures or SLB (see Q5), so retail mean reversion is realistically long-only in cash or ETFs, or long/short via futures in about 200 F&O stocks.

### Gaps
- No India-specific RSI(2), Bollinger-band or short-term (1-week/1-month) reversal study with after-cost results was found, and no evidence on how such edges have decayed in India.
- No Quantified Strategies or Zerodha Varsity backtest on Nifty or BankNifty mean reversion was found in this session.

---

## 4. Intraday equity strategies (ORB, VWAP, gap trading): after-cost evidence for retail; SEBI's intraday study

### Takeaway
There is no credible, independent after-cost evidence that intraday ORB, VWAP or gap strategies are profitable for Indian retail traders. SEBI's own data shows 71% of individual intraday cash traders lost money in FY23, rising to 80% for the most active. Meanwhile, almost all profits made by FPIs and proprietary desks in F&O came from algorithmic trading. Retail intraday algos compete against those desks.

### Cited Findings
- SEBI study released 24 Jul 2024, covering FY2022-23 — [SEBI press release](https://www.sebi.gov.in/media-and-notifications/press-releases/jul-2024/sebi-study-finds-that-7-out-of-10-individual-intraday-traders-in-equity-cash-segment-make-losses_84948.html); [Business Standard](https://www.business-standard.com/amp/markets/news/over-70-intra-day-traders-incur-losses-during-fy23-reveals-sebi-study-124072401110_1.html); [Moneylife](https://moneylife.in/article/7-out-of-10-individual-intraday-traders-in-equity-cash-segment-make-losses-sebi-study/74733.html):
  - 71% of individual intraday traders in the equity cash segment made net losses.
  - 80% of those with more than 500 trades a year made losses.
  - 76% of traders under 30 made losses.
  - The number of individual intraday traders rose more than 300% from FY19 to FY23.
  - The sample covered the top-10 brokers, about 86% of individual clients.
  - Average loss was about ₹5,371 (secondary reports).
- SEBI F&O study — [Moneylife](https://www.moneylife.in/article/93-percentage-of-individual-traders-lost-rs18-lakh-crore-in-equity-fo-in-past-3-years-sebi/75210.html); [Wright Research summary](https://wrightresearch.in/blog/sebi-futures-and-option-report-individual-traders-in-fandos-incur-rs-18-lakh-crore-loss-over-3-years):
  - In FY24, proprietary traders made about ₹33,000 crore and FPIs about ₹28,000 crore in gross profits.
  - 97% of FPI profits and 96% of proprietary-trader profits came from algorithmic trading.
  - 93% of more than 1 crore individual F&O traders lost money, averaging about ₹2 lakh each over the three years (FY22–FY24). Only 1% made more than ₹1 lakh after costs.
- [ACADEMIC, US] Gao, Han, Li & Zhou found that the first half-hour return of the S&P 500 ETF (1993–2013) predicts the last half-hour return. The effect is stronger on volatile, high-volume and macro-news days — [Alpha Architect summary](https://alphaarchitect.com/2014/08/attention-prop-traders-the-first-half-hour-of-trading-predicts-the-last-half-hour/). A Reading working paper finds intraday time-series momentum significant across international markets, but India's inclusion was not confirmed — [Reading accepted version](https://reading-9.eprints-hosting.org/95566/1/Accepted-Version.pdf)
- [PRACTITIONER] An Indian ORB guide says disciplined traders stick to the index and the top 50–100 stocks by volume, because thin stocks give "jagged, untradeable ranges". STT plus brokerage "materially shrink small intraday wins" — [OneTradeJournal ORB](https://onetradejournal.com/strategies/opening-range-breakout); [15-min ORB](https://onetradejournal.com/strategies/fifteen-minute-orb-strategy)
- [VENDOR, unverified] A Nifty 50 open-high/open-low scanner claims a 55–58% win rate at 1:1.3 risk-reward for a long-only setup, with no methodology or costs disclosed — [skill readme](https://skillselion.com/skills/drdivs/notsosebi-trading-skills/ohl-breakout-scanner)
- Zerodha's "In The Money" ran a time-based ORB series on the Nifty index. The search snippets showed no results or cost assumptions — [Zerodha Z-Connect](https://zerodha.com/z-connect/?p=395201) (link from search; content not verified)

### Inferences
- The SEBI numbers show that the median retail intraday trader loses, and that losses rise with activity. That is consistent with cost drag dominating any small edge. A Kite Connect ORB/VWAP bot multiplies trade count, so it would need a demonstrated gross edge well above roughly 0.05–0.1% per round trip. This threshold is an unsourced estimate.
- The SEBI F&O finding that 96–97% of institutional F&O profits come from algos implies that intraday edges are already being harvested by co-located HFT and prop desks. Retail algos at Kite Connect API latency are unlikely to compete on microstructure edges.

### Gaps
- No peer-reviewed or audited study of ORB, VWAP-reversion or gap-fill strategies on NSE stocks with realistic costs was found.
- Could not open the SEBI intraday PDF to confirm the breakdown of trading costs as a share of losses (often quoted from the study but not verified here).
- The current STT, exchange and stamp-duty schedule for intraday equity and futures was not verified in this session. It should be checked on NSE or broker charge pages before modelling costs.

---

## 5. Pairs trading / statistical arbitrage in India: studies, half-lives, breakdown risk, shorting and lot-size constraints

### Takeaway
The strongest Indian evidence, a 2011–2017 thesis, found futures-based pairs trading significantly profitable after costs (up to about 34% annualised) while cash-market pairs were not. Most other studies are small, short-window arXiv papers with wide half-life ranges and visible breakdown risk. For retail, the binding constraints are practical: overnight shorts need futures or SLB, and futures lot sizes run to several lakh per leg, rising to ₹15–20 lakh for index contracts.

### Cited Findings
- [ACADEMIC] A 2011–2017 study of statistical arbitrage in Indian markets formed pairs on a rolling basis using distance and cointegration methods. Pairs trading in stock futures was "significantly profitable", with average annualised profitability of up to 34% including transaction costs. Spot-market pairs were not profitable. Commodity pairs reached up to 59% average annualised profitability — [Krishikosh (thesis repository)](https://krishikosh.egranth.ac.in/items/79c40268-bdee-41b3-8d31-c9998a994d25/full)
- [ACADEMIC] Sen (arXiv 2211.07080) formed pairs from five NSE sectors using 2018–2020 prices and tested them on 2021. Auto and realty pairs did best; 2 of 5 IT pairs had negative returns. It is a single test year with a small sample — [arXiv](https://arxiv.org/pdf/2211.07080)
- [ACADEMIC] An ESG pairs paper on Indian stocks (arXiv 2401.14761) reports cointegrated pairs with half-lives from about 62 to about 4,966 (in the table's units). One pair (JINDALPOLY–RCOM) has a negative half-life, meaning no mean reversion — [arXiv](https://arxiv.org/pdf/2401.14761)
- [ACADEMIC] A cointegration-plus-clustering study used the top 10 free-float stocks in 12 NSE sectors, with 2018–2021 formation and 2022 testing. Return figures were not extracted — [Authorea](https://authorea.com/users/691568/articles/682160-a-cointegration-and-clustering-based-approach-to-pair-trading-of-stocks-from-selected-sectors-of-the-indian-stock-market)
- [ACADEMIC] Mahajan & Chandra ran Johansen cointegration tests on MCX spot commodity prices with a train/test split — [EconPapers](https://econpapers.repec.org/paper/arxpapers/1907.08397.htm)
- Shorting rules — [Zerodha Z-Connect on shorting](https://zerodha.com/z-connect/trending/shorting-and-indian-capital-markets); [Strike.money STBT/short rules](https://www.strike.money/stock-market/stbt):
  - Retail cash-market shorts are intraday only.
  - Overnight shorts need SLB (introduced 2008; activity picked up only after 2018, when rollover of up to 12 months was allowed) or a short futures position.
  - Naked shorting is prohibited.
- SEBI's chair has announced a review of short-selling rules; scope and timeline unknown — [Outlook Money](https://www.outlookmoney.com/invest/sebi-chief-tuhin-kanta-pandey-announces-short-selling-review-what-it-means-for-retail-investors)
- Lot sizes — [Fyers notice](https://fyers.in/notice-board/sebis-revised-lot-sizes-for-index-derivatives-effective-november-20-2024/); [Zerodha bulletin](https://zerodha.com/marketintel/bulletin/411352/revision-in-lot-size-of-index-derivative-contracts-from-april-25-2025):
  - SEBI's 1 Oct 2024 circular requires new index derivatives to have a contract value of at least ₹15 lakh, with lots set to ₹15–20 lakh on review.
  - Nifty lot size went from 25 to 75 and Bank Nifty from 15 to 30, effective 20 Nov 2024.
  - Bank Nifty then moved to 35 and Midcap Select to 140 from 25 Apr 2025.

### Inferences
- A retail pairs trade held overnight on Kite Connect needs both legs in stock futures, or a long-cash plus short-futures structure. Lot granularity forces imperfect hedge ratios, and pair candidates are limited to F&O-eligible stocks (about 200 names).
- Breakdown risk is real. The ESG paper's RCOM pair involved a company that later went through insolvency (general knowledge, not sourced here), and half-lives in the thousands of days mean many "cointegrated" pairs are not tradeable.
- The futures-only profitability in the 2011–2017 study likely reflects cheaper futures transaction costs and easier shorting. The study predates the 2024 rise in futures STT and lot sizes, so its after-cost returns probably overstate today's results.

### Gaps
- Current single-stock futures contract-value rules and typical lot values in 2025–2026 were not found.
- No study measuring pair half-lives against realised returns in India, or pair breakdown rates over 2020–2026, was found.
- SLB borrow fees and availability for retail via Zerodha were not quantified.

---

## 6. Cash-futures arbitrage: arbitrage fund returns (1/3/5 years), basis spreads, practicality for ₹1 lakh retail

### Takeaway
Arbitrage mutual funds earned category averages of about 6.2–6.5% (1Y), 7.2–7.3% (3Y) and 6.5% (5Y) as of Aug–Sep 2026 (direct plans), with calendar-year returns of 4.1–8.1% from 2021 to 2025. DIY cash-futures arbitrage with ₹1 lakh is impractical: one stock-futures lot typically needs several lakh rupees, and retail round-trip costs of about 0.2–0.4% of notional consume most of a typical monthly basis. An arbitrage fund or liquid ETF is the efficient way to hold this exposure.

### Cited Findings
- [LIVE] The arbitrage category's 1Y average was 6.18% (7 Aug 2026), 6.55% (24 Aug 2026) and 6.49% (10 Sep 2026). The 3Y average was 7.15–7.27% — [arthgyaan Tata vs Sundaram](https://arthgyaan.com/fund/compare/tata-arbitrage-fund-direct-growth-vs-sundaram-arbitrage-fund-direct-growth/145724-vs-149550); [arthgyaan DSP vs Tata](https://arthgyaan.com/fund/compare/dsp-arbitrage-fund-direct-growth-vs-tata-arbitrage-fund-direct-growth/142283-vs-145724); [arthgyaan Kotak vs Union](https://arthgyaan.com/fund/compare/kotak-arbitrage-fund-direct-growth-vs-union-arbitrage-fund-direct-growth-option/119771-vs-146297)
- [LIVE] The 5Y category average was 6.49–6.52% (Aug 2026). Individual 5Y returns: ABSL 6.82%, Edelweiss 6.82%, Tata 6.77%, ICICI Pru 6.70%, UTI 6.62%, Union 6.49%, JM 6.34% — [arthgyaan ABSL](https://arthgyaan.com/fund/aditya-birla-sun-life-arbitrage-fund-direct-growth/119526); [arthgyaan ICICI](https://arthgyaan.com/fund/icici-prudential-arbitrage-fund-direct-growth/120364)
- [LIVE] Calendar-year category returns: 2021 4.10%, 2022 4.66%, 2023 7.62%, 2024 8.06%, 2025 6.89%, 2026 YTD 3.61% (partial year) — [arthgyaan arbitrage category](https://arthgyaan.com/funds/categories/arbitrage-hybrid-funds)
- Tax treatment per the fund pages: short-term gains (held under 1 year) taxed at 20%; long-term gains at 12.5% above ₹1.25 lakh a year (equity taxation) — [arthgyaan Tata](https://arthgyaan.com/fund/tata-arbitrage-fund-direct-growth-option/145724)
- IIMB research: STT is the largest cost component and "a kind of spoilsport" for arbitrage. Opportunities concentrate in heavily traded contracts such as Nifty and Reliance, and for small participants costs often exceeded the excess premium — [IIMB repository](https://repository.iimb.ac.in/handle/2074/18746); [Tejas@IIMB](https://tejas.iimb.ac.in/articles/66.php)
- [PRACTITIONER] Break-even is about 0.2% round trip (round-trip charges divided by share price). Retail costs typically run 0.20–0.40% of notional per round trip for liquid F&O stocks. Funding via broker margin (about 12–18% a year) kills most trades. Dividend months can shrink or invert the basis — [OneTradeJournal cash-and-carry](https://onetradejournal.com/strategies/cash-and-carry-arbitrage); [OneTradeJournal arbitrage cost math](https://onetradejournal.com/glossary/arbitrage); [EquitiesIndia](https://equitiesindia.com/learn/derivatives/futures-arbitrage-india)
- [PRACTITIONER] A worked example puts net returns at about 5–7% annualised, with about ₹7–7.5 lakh needed per single-stock arbitrage position — broker-education source in search results ([Angel One podcast](https://www.angelone.in/podcast/cash-future-arbitrage) / [5paisa](https://www.5paisa.com/articles/cash-and-carry-arbitrage); exact attribution not verified)

### Inferences
- With ₹1 lakh, a retail trader cannot open even one hedged single-stock futures lot, and index futures need ₹15–20 lakh notional. DIY arbitrage is not feasible at that size. Arbitrage funds (about 6.5–7% pre-tax, equity taxation, no lot constraints) dominate for small capital.
- Arbitrage returns tracked short-term rates and were not hurt by the 2025–2026 equity weakness. Calendar 2024 (8.06%) was the best year in the series, when bullish leverage demand widened futures premia.
- For an algo system, an arbitrage fund or liquid ETF is the natural "cash/risk-off" leg for momentum or trend strategies.

### Gaps
- No source gave actual Nifty or stock-futures basis spreads (annualised monthly roll yield) for 2025–2026.
- Category data comes from a single aggregator (arthgyaan, direct plans). AMFI, Value Research and Morningstar category averages were not cross-checked.
- The current STT on futures and delivery after the 2024 budget changes was not verified in this session.

---

## 7. Multi-asset / dual momentum allocation (Nifty, midcap, gold, silver, international ETFs, liquid ETFs)

### Takeaway
Several Indian practitioner backtests of Nifty/gold dual momentum report a 16–19% CAGR versus 12–13% for the Nifty, with max drawdowns around 23%. Capitalmind finds returns comparable to the Nifty with lower volatility. All of these are blog-quality backtests with differing rules, and none is audited. 2025–2026 was a favourable regime: precious metals far outran equities, so a relative-momentum switch would plausibly have held gold or silver for much of the period. That conclusion is inferred, not backtested here.

### Cited Findings
- [BACKTEST] Samasthiti's rule compares each asset's 200-day return against the other asset and a 200-day FD return, and parks in FD when neither beats it. Over 2014–2024 it reports a CAGR of 18.79% versus 12.13% for the Nifty and 10.86% for gold — [Samasthiti substack](https://samasthiti.substack.com/p/indian-edition-of-the-dual-momentum)
- [BACKTEST] A quarterly rule holding whichever of NIFTYBEES or GOLDBEES had the better 3-month return reports a CAGR of 16.06%, total return of 1,221.5% and max drawdown of -23.51% over 14 years. The author ran the test with ChatGPT, so methodology is unverified — [TradingQnA](https://tradingqna.com/t/dual-momentum-strategy-with-niftybees-goldbees/174470)
- [BACKTEST] Capitalmind concludes that a Nifty–gold dual momentum switch offers returns comparable to the Nifty with lower volatility, and notes gold's long-term returns trail the Nifty — [Capitalmind](https://premium.capitalmind.in/2022/06/should-gold-be-in-your-long-term-portfolio/)
- [BACKTEST] StockViz's equal-weight Nifty plus gold trend system halved validation drawdown (about 10% versus 20%) — [Zerodha Varsity Part II](https://zerodha.com/z-connect/varsity/could-trend-following-be-a-successful-trading-strategy-part-ii)
- Another dual momentum backtest (Momentum Lab) and a live dual-momentum smallcase exist. No figures were extracted — [Momentum Lab](https://momentumlab.substack.com/p/backtesting-dual-momentum-strategy); [smallcase BENMO_0001](https://www.smallcase.com/smallcase/BENMO_0001)
- Regime data: see Q2. Gold +72% and silver +122% versus Nifty 500 +7% in 2025; Nifty -14.4% YTD in 2026 (to mid-Oct); gold +28% over 1Y to 30 Sep 2026. The 5-year-low Nifty/gold ratio (1.62, Apr 2026) was flagged as a heuristic that has historically preceded equity rallies — [share.market](https://www.share.market/buzz/insights/the-nifty-to-gold-ratio-a-compass-for-investors-in-times-of-war-and-market-volatility/)

### Inferences
- Dual momentum's edge in India comes mostly from occasional long gold regimes (2008, 2011–12, 2019–20, 2025–26) during equity drawdowns. Results depend heavily on lookback (90 vs 200 days) and rebalance frequency, and the two backtests above disagree by about 2.7 pp CAGR. Expect lookback-selection overfitting.
- It is implementable via Kite Connect using ETFs (NIFTYBEES, mid-cap ETFs, GOLDBEES, SILVERBEES, LIQUIDBEES) with ₹1 lakh. Costs are low, but each switch realises gains taxed at STCG or LTCG rates, which none of the backtests model.
- A switch into gold/silver after the 2025 rally carried mean-reversion risk, as the Aug–Sep 2026 metals pullback showed.

### Gaps
- No backtest including silver, midcap, international ETFs or liquid ETFs as separate assets was found.
- Practical issues with international ETFs in India (RBI overseas-investment limits causing ETF premiums to NAV) were not researched.
- No live (audited) dual-momentum fund track record in India was found.

---

## 8. Market-neutral / long-short evidence in India (SEBI 2025 SIF long-short funds, Category III AIF long-short)

### Takeaway
Live long-short evidence is short and dispersed. Equity long-short SIFs (launched from late 2025 under SEBI's SIF framework) were down 1.8% YTD to 15 Oct 2026, versus a Nifty about 14% lower. Their 59% downside capture in the Q1 2026 fall compares with 90–92% for large-cap and flexi-cap mutual funds. Since-launch returns vary widely, from about -6% to +11%. Category III long-short AIFs have trailed long-only AIFs over 2–3-year windows on the limited data found. Neither vehicle shows a clear, persistent market-neutral edge yet, and both require ₹10 lakh+ minimums (not verified here) rather than retail algo capital.

### Cited Findings
- [LIVE] Ionic Wealth study, YTD to 15 Oct 2026: equity long-short SIFs -1.8%, equity ex-top-100 long-short SIFs +13.1%. In the Jan–Mar 2026 fall, equity long-short SIFs had a downside capture ratio of 59%, versus 92% for large-cap and 90% for flexi-cap mutual funds — [5paisa](https://www.5paisa.com/index.php/blog/sif-performance-data-shows-wide-gap-across-long-short-strategies-in-2026); see also [INDmoney](https://www.indmoney.com/blog/mutual-funds/sif-returns-are-surging) (the search summary did not say which page carries the Ionic data)
- [LIVE] Since-launch absolute returns to 22 Jul 2026 for nine equity long-short SIFs (ACE MF data): qsif about 10.85%, DynaSIF about 6.33%, Arudha about 4.70%, iSIF about 3.50%, Titanium about 3.26%, Arthaya about -0.15%, Sapphire about -0.13%, Diviniti about -6.21%. Several have only months of history, and table rows are misaligned in places — [Upstox](https://upstox.com/news/personal-finance/mutual-funds/equity-vs-hybrid-long-short-si-fs-how-have-20-funds-performed-since-launch-july-2026/article-197453/)
- [LIVE] Crisil AIF Index (Cat III, INR): 1Y return 9.86% to Mar 2025, and -8.76% calendar-YTD to Mar 2025. Category III includes long-only, long-short, hybrid and other sub-categories — [Marcellus benchmark report, Mar 2025](https://marcellus.in/wp-content/uploads/2026/02/Benchmark-Report_Marcellus-Investment-Managers-Private-Limited_Cat-III_Mar-2025.pdf)
- Long-short strategies make up about 26% of more than 500 Cat III schemes; long-only about 70% (Aug 2025) — [Business Standard](https://www.business-standard.com/amp/markets/news/category-iii-aifs-take-leap-in-interest-from-hnis-family-offices-125080701823_1.html)
- [LIVE] An IVCA report puts the FY25 median return of equity Cat III AIFs at 26% (top quartile above 40%, bottom quartile 5%). It blends long-only and long-short. A trailing NSE-benchmark snapshot (undated) shows long-short equity at 16.46% (3Y) and 10.12% (2Y), versus long-only at 27.91% (3Y) and 9.45% (2Y), with Cat III overall at 23.30% (3Y) — reported in search results from [iVentures](https://iventures.in/feeds/blog/aif-returns) / [Finnovate](https://www.finnovate.in/learn/blog/aif-category-iii-india) (exact attribution and as-of date not verified); NSE benchmark reports at [NSE AIF benchmark](https://www.nseindia.com/products-services/aif-benchmark-report)
- Wealthy investors have been shifting from MFs and PMS to Cat III AIFs as a volatility hedge — [Nuvama press release](https://www.nuvama.com/media-archive/press-releases/wealthy-investors-shift-from-mfs-pms-to-cat-iii-aifs-in-hedge-against-volatility/)

### Inferences
- In 2026's falling market, long-short SIFs cut losses substantially (about -2% versus about -14% for the Nifty) but were not truly market-neutral. The gap between ex-top-100 (+13.1%) and broad equity long-short (-1.8%) shows manager and segment dispersion matters more than the long-short label.
- The pooled vehicles' main structural advantage over a retail algo trader is shorting via derivatives at scale. A ₹1 lakh retail account cannot replicate a market-neutral book because single-stock futures lots are several lakh and index lots ₹15–20 lakh.
- Survivorship: SIF and AIF league tables cover only surviving schemes, and AIF returns are often self-reported or benchmarked with a lag.

### Gaps
- The SEBI SIF framework details (₹10 lakh minimum investment; unhedged short exposure cap of about 25% via derivatives) were not verified with a primary SEBI source in this session.
- No clean calendar-2025 or 2026 return for the Cat III long-short sub-category was found. Check NSE AIF benchmark or Crisil AIF reports, or PMS Bazaar.
- No audited Indian equity market-neutral (beta about 0) fund track record was found.
