# Who Profits from Trading in India, Why, and What Is Realistic for a Skilled Small-Account (Algo) Trader

Research notes as of 2026-10-29. Method note: www.sebi.gov.in and faculty.haas.berkeley.edu could not be fetched from this research environment (blocked by the network allowlist). So SEBI study figures come from reputable secondary coverage (Business Standard, BusinessToday, CNBC and others) and the SEBI X account, not the PDFs themselves. Where sources disagree this is flagged. Computations marked "my calculation" were done in Python and are reproducible from the formulas given.

## 1. Who makes money in Indian F&O, and the role of algos, HFT/market makers and the Jane Street order

### Takeaway
In every SEBI study since 2023, roughly 7 to 9 in 10 individual F&O traders lose money: 93% over FY22–FY24, about 91% in FY25 and 87.7% in FY26. The aggregate gains go to proprietary desks and FPIs, and about 96–97% of their FY24 profits came from algorithmic trading. The Jane Street order shows how large these gains can be for a well-capitalised, low-latency, cross-market player: about ₹36,500–36,700 crore of net trading gains in about 27 months. It also shows that the regulator can claw back part of them.

### Cited Findings
**SEBI FY22–FY24 study (released 23 Sep 2024)**
- 93% of over 1 crore individual F&O traders lost money over FY22–FY24, with an average loss of about ₹2 lakh per trader including transaction costs. Aggregate individual losses exceeded ₹1.8 lakh crore over the three years. Only 1% of individual traders made profits above ₹1 lakh after transaction costs. — [BusinessToday](https://www.businesstoday.in/markets/story/93-of-individual-traders-incurred-losses-in-equity-fo-during-fy22-fy24-sebi-study-447102-2024-09-23); [Benzinga](https://www.benzinga.com/24/09/40994647/sebi-study-unveils-93-of-individual-f-o-traders-suffered-losses-between-fy22-and-fy24)
- In FY24, proprietary traders made the highest **gross** profit (before transaction costs) in NSE equity F&O, about ₹33,000 crore. FPIs followed with about ₹28,000 crore. About 97% of FPI profits and 96% of proprietary-trader profits came from algorithmic trading. Only about 13% of individual traders used algos, and even that figure is overstated because it includes broker-forced square-offs executed by algo. — [BusinessToday](https://www.businesstoday.in/markets/story/93-of-individual-traders-incurred-losses-in-equity-fo-during-fy22-fy24-sebi-study-447102-2024-09-23); [Zerodha TradingQnA summary](https://tradingqna.com/t/sebis-latest-analysis-of-profits-losses-in-the-equity-derivatives-segment-fy22-fy24/173596)
- Secondary sources say "about 7.2%" of individuals were profitable over FY22–FY24 and that individuals paid about ₹50,000 crore in transaction costs (51% brokerage, 20% exchange fees). These are derived or unverified numbers and should not be quoted as SEBI figures. — [disciplinetrade.com](https://disciplinetrade.com/research/sebi-fo-traders-study/); [arthalearn](https://www.arthalearn.com/blog/sebi-study-93-percent-fno-traders-lose)

**SEBI FY25 study (released 7 Jul 2025)**
- More than 91% of individual traders lost money in equity derivatives in FY25, broadly unchanged from the previous study. Individuals' net losses after transaction costs rose to ₹1,05,603 crore in FY25, from ₹74,812 crore in FY24 (about +41%). The sample covered the top 13 brokers, about 96 lakh unique traders. — [Business Standard](https://www.business-standard.com/amp/markets/news/net-losses-of-traders-in-fo-widens-in-fy25-sebi-study-125070701221_1.html); [InvestWhat](https://www.investwhat.in/india/investment/investor-news/25062/91-lose-rs106-lakh-crore-written-off-whats-going-on-in-indias-fo-arena)

**SEBI FY25–FY26 study (released Aug 2026)**
- 87.7% of individual traders had net losses in FY26. Aggregate losses fell about 18% to ₹91,685 crore. About 92% of aggregate losses came from options. The average loss per trader rose slightly to about ₹1.17 lakh. The study covers about 90% of individual traders in the segment. — [Business Standard, Aug 2026](https://www.business-standard.com/markets/news/active-derivatives-traders-fall-18-in-fy26-to-8-75-million-sebi-study-126082001378_1.html); [Finnovate](https://www.finnovate.in/learn/blog/sebi-fno-trader-losses-fy26-individual-derivatives); [SEBI on X](https://x.com/SEBI_updates/status/2090451964626894921); [PeoplePlus](https://www.peopleplus.press/en/business/stock-market/details/sebi-study-877-percent-of-individual-fo-traders-lost-money-in-fy26-as-options-drove-most-losses)
- **Conflict on headcount:** SEBI's X post and Business Standard say active traders fell 18% from 106.2 lakh (FY25) to 87.5 lakh (FY26). Other sources say they fell from 98.1 lakh to 78.6 lakh. The FY25 figures were also restated because the broker sample grew from 13 to 15. — [Business Standard](https://www.business-standard.com/markets/news/active-derivatives-traders-fall-18-in-fy26-to-8-75-million-sebi-study-126082001378_1.html); [CorpLawUpdates](https://www.corplawupdates.in/updates/sebi-equity-derivatives-retail-trader-study-fy26); [FinTechBizNews](https://fintechbiznews.com/govtregulators/sebi-released-2-analytical-studies)

**SEBI intraday cash-equity study (Jul 2024, data for FY23)**
- 71% of individual intraday traders in the equity cash segment had a net loss in FY23. The share of loss-makers rose to 80% among very frequent traders (more than 500 trades a year). Loss-makers placed more trades on average than profit-makers. 76% of traders under 30 were loss-makers. Loss-makers spent an extra 57% of their trading losses on trading costs. The sample covered about 7 million investors at the top 10 brokers. — [Business Standard](https://www.business-standard.com/amp/markets/news/7-in-10-intraday-traders-in-equity-cash-suffered-losses-in-fy23-sebi-study-124072400975_1.html); [Business Standard (2)](https://www.business-standard.com/amp/markets/news/over-70-intra-day-traders-incur-losses-during-fy23-reveals-sebi-study-124072401110_1.html); [Angel One summary](https://www.angelone.in/news/market-updates/sebi-highlights-intraday-trading-risk)

**Algo, co-location and HFT share**
- Algorithmic trading accounted for about 69% of NSE equity-derivatives turnover and about 54% of cash turnover in Q1 FY26 (from NSE disclosures). Other estimates put it at 66% of derivatives in FY26, and NSE Market Pulse is cited at about 70% for 2024-25 (notional). — [Multibagg (NSE RHP data)](https://www.multibagg.ai/market-pulse/articles/ipo/nse-algorithmic-trading-derivatives-turnover-rhp-cmufcpv210014bznvcom3hnfk); [OpenAlgo blog](https://blog.openalgo.in/state-of-algo-trading-in-india-2026-rules-platforms-costs-91fcc19a0d20)
- Co-location (servers inside the exchange) is reported to account for 62.1% of equity-derivatives turnover in 2024, up from 7.3% in 2010. On a premium-turnover basis it is reported at 49.5% of equity futures and 53.6% of equity options turnover. This is a secondary figure, and the article's headline numbers (35.7% co-location, 53% algo) appear to refer to a different segment. — [Investing.com India](https://in.investing.com/news/colocation-hits-357-algo-trading-surges-to-53-the-techdriven-shift-in-nse-4655643)
- NSE's published "algo" category is broad: FPIs, prop desks, HFTs, co-location and DMA users, and retail API users. It is not split into HFT/market-maker flow versus other flow. — [OpenAlgo blog](https://blog.openalgo.in/state-of-algo-trading-in-india-2026-rules-platforms-costs-91fcc19a0d20)

**Jane Street interim order (3 Jul 2025)**
- SEBI barred Jane Street group entities from the securities market and impounded ₹4,843.57 crore as alleged unlawful gains. It found manipulative strategies on 21 expiry days. This was described as possibly SEBI's largest-ever disgorgement direction. — [Business Standard](https://www.business-standard.com/markets/news/sebi-bars-jane-street-orders-rs-4844-cr-disgorgement-market-manipulation-125070400081_1.html); [Mondaq](https://www.mondaq.com/india/commoditiesderivativesstock-exchanges/1648134/sebis-interim-order-against-jane-street-allegations-of-index-manipulation-explained); [CNBC](https://www.cnbc.com/2025/07/04/indian-regulator-bars-us-trading-firm-jane-street-from-accessing-securities-market.html)
- **Scale of gains, Jan 2023–Mar 2025:** Business Standard reported ₹44,358 crore of gains in options, offset by losses of ₹7,208 crore in stock futures, ₹191 crore in index futures and ₹288 crore in cash, for a net gain of ₹36,671 crore. Other accounts give index-options gains of ₹43,289.33 crore, cumulative other-segment losses of ₹7,687.21 crore and a net of about ₹36,500 crore (about US$4.3bn). WION gives options profit of "over ₹43,000 crore ($5.16bn)". — [Business Standard](https://www.business-standard.com/markets/news/sebi-bars-jane-street-orders-rs-4844-cr-disgorgement-market-manipulation-125070400081_1.html); [Parth Malpani analysis](https://parthmalpani.medium.com/jane-street-india-market-manipulation-case-analysis-c8e39ea1bc34); [WION](https://www.wionews.com/business-economy/jane-street-banned-in-india-why-sebi-cracked-down-on-the-wall-street-giant-1751784750472/amp)
- **Alleged mechanism:** On expiry days the group bought large amounts of Bank Nifty constituent stocks and futures early in the session while building large short or bearish index-options positions. It then sold the cash and futures positions later in the day, pushing the index down and raising the value of the options book. SEBI cited PFUTP Regulations 3 and 4(2)(a), (b), (e), (g). — [Mondaq](https://www.mondaq.com/india/commoditiesderivativesstock-exchanges/1648134/sebis-interim-order-against-jane-street-allegations-of-index-manipulation-explained); [CNBC (18 Jul 2025)](https://www.cnbc.com/2025/07/18/jane-street-sebi-arbitrage-become-market-manipulation-mens-re-derivative-india-markets.html)
- Jane Street says the trades were standard "index arbitrage", not manipulation. Analyses of the order say the pattern continued on expiry days into May 2025 despite NSE caution letters in February 2025 (secondary reporting). — [CNBC](https://www.cnbc.com/2025/07/18/jane-street-sebi-arbitrage-become-market-manipulation-mens-re-derivative-india-markets.html); [DataIntellect](https://dataintellect.com/blog/sebi-vs-jane-street-index-manipulation-scandal-and-a-regtech-wake-up-call/)
- Jane Street deposited the impounded amount into escrow in July 2025. One report prints the figure as ₹4,834.6 crore, likely a transposition of ₹4,843.6 crore. — [India News Network](https://www.indianewsnetwork.com/en/20250715/jane-street-transfers-4-834-6-crore-to-sebi-amid-market-manipulation-allegations)
- **Status as of Oct 2026:** At a Securities Appellate Tribunal hearing (reported 6 Oct 2026), SEBI said it had shared more than 10 GB of data with Jane Street. SEBI's counsel said the interim order could "probably be vacated" if Jane Street shows its trading was not manipulation. The case is not finally decided. — [BusinessToday](https://www.businesstoday.in/markets/story/sebi-tells-sat-that-jane-street-has-enough-data-to-respond-to-market-manipulation-charges-559953-2026-10-06)

### Inferences
- Index options are close to zero-sum before costs and negative-sum after them. Year after year, individuals lose ₹75,000–1,05,000 crore while prop desks and FPIs book tens of thousands of crores in gross profit, almost all of it algorithmic. This is consistent with a transfer from directional, retail option buyers and sellers to market makers, HFT arbitrageurs and well-capitalised cross-market players. Exchanges, brokers and the government also take a fixed toll (STT, brokerage, exchange fees, GST).
- The edges the winners hold are structural, not "better chart reading": co-located low-latency infrastructure (a majority share of derivatives turnover), the ability to quote two-sided and earn the spread, very large balance sheets that let them trade cash, futures and options together (the heart of the Jane Street case), cheaper per-unit costs, and dedicated risk teams. A retail API algo running through a broker has none of these, so it cannot compete with HFTs at the speed or market-making layer.
- The Jane Street figures (net about ₹36,600 crore in about 27 months) set the upper bound of what a top global firm extracts from Indian index options. Even there, SEBI treated about ₹4,844 crore (roughly 13%) as allegedly unlawful, which shows the regulatory risk around expiry-day strategies.
- SEBI's late-2024 and 2025 curbs reduced participation and losses in FY26 (87.7% loss-makers, ₹91,685 crore of losses), but the loss rate is still near 9 in 10.

### Gaps
- The exact FY25 and FY26 prop/FPI profit figures and algo shares could not be verified from the SEBI PDFs (sebi.gov.in was blocked). One unattributed secondary snippet said proprietary traders earned about ₹44,000 crore gross and FPIs about ₹14,000 crore in the FY25–26 study, and another said "99% of FPI/prop profits were made by algo entities". Both are unverified.
- There is no public SEBI or NSE split of profits between HFT/market makers and other prop algos, and no data on exchange rebates or market-maker incentives captured by specific firms.
- The FY26 headcount conflict (87.5 lakh vs 78.6 lakh) is unresolved.

## 2. Global academic evidence on retail day-trader performance

### Takeaway
The largest datasets (Taiwan, all trades 1992–2006; Brazil, all mini-index futures day traders) find that **fewer than 1%** of day traders predictably earn positive abnormal returns after fees, and **97%** of those who persist for 300+ days lose money. Even the best persistent traders earn modest absolute amounts, and losers keep trading.

### Cited Findings
- **Barber, Lee, Liu & Odean, "The Cross-Section of Speculator Skill: Evidence from Day Trading", *Journal of Financial Markets* 18(1), 2014.** Using Taiwan Stock Exchange data from 1992 to 2006, they conclude that **less than 1% of the day-trader population can predictably and reliably earn positive abnormal returns net of fees**. Traders are ranked on prior-year returns. The top 500 then earn **61.3 bps/day before fees and 37.9 bps/day after fees** the next year, while bottom-ranked traders earn −11.5 bps before and −28.9 bps after. An earlier 2011 draft reports 49.5/28.1 bps for the top 500. — [eScholarship](https://www.escholarship.org/uc/item/7k75v0qx); [SSRN](https://dx.doi.org/10.2139/ssrn.529063)
- **Barber, Lee, Liu & Odean, "Learning, Fast or Slow", *Review of Asset Pricing Studies* 10(1), 2020.** Aggregate day-trader performance is negative. **74% of day-trading volume comes from traders with a history of losses**, and **97% of day traders are likely to lose money in future day trading** (a model-based projection, not an observed share). Unprofitable traders are more likely to quit than profitable ones, but many persist, which the authors read as overconfidence and biased learning rather than rational learning. The data covers 3.7 billion TWSE transactions from 1992 to 2006. — [EconPapers abstract](https://econpapers.repec.org/article/ouprasset/v_3a10_3ay_3a2020_3ai_3a1_3ap_3a61-93..htm); [AEA 2019 conference listing](https://www.aeaweb.org/conference/2019/preliminary/paper/ZKnGb4Zh)
- A secondary summary of the same paper says 95.3% of previously unprofitable traders with 50 or more day-trading days kept trading over the next 12 months. It also says about 450,000 individuals day-traded in an average year, and that the study focuses on about 277,000 who traded more than NT$600,000 (about US$20k) a year. — [Tradicted summary](https://www.tradicted.com/research/barber-learning-2020/); [Tradewink](https://www.tradewink.com/learn/how-many-day-traders-are-profitable)
- **Chague, De-Losso & Giovannetti, "Day Trading for a Living?" (2019/2020 working paper, FGV/SSRN).** All 19,646 individuals who began day trading mini-Ibovespa futures in 2013–2015 were tracked. Among those who persisted for 300 or more days, **97% lost money**. **Only 1.1% earned more than the Brazilian minimum wage, and only 0.5% (0.4% in the FGV version) earned more than a bank teller's starting salary (about US$54/day).** The best individual earned only **US$310/day with a daily standard deviation of US$2,560**. There was **no evidence of learning**: performance does not improve with experience. — [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3423101); [FGV repository](https://repositorio.fgv.br/items/e87d04fc-4b4c-4a56-ab5a-1c84c1afde1b/full); [CXO Advisory](https://www.cxoadvisory.com/investing-expertise/day-trading-a-bust/)
- The Brazil authors caution that their sample may not represent other countries or assets. Some Brazilian press reports describe the sample differently (98,378 people starting 2013–2016, 554 persisting more than 300 sessions), which reflects a different window. — [CXO Advisory](https://www.cxoadvisory.com/investing-expertise/day-trading-a-bust/); [Money Times](https://www.moneytimes.com.br/ganho-no-day-trade-nao-bate-salario-minimo-no-brasil/)

### Inferences
- Across Taiwan, Brazil and India (SEBI: 71% of intraday cash traders and 87.7–93% of F&O traders lose money in a given period), the fraction **consistently** profitable after costs over several years is at most low single digits, and in the Taiwan and Brazil studies under 1%. India's single-year "profitable" shares of 7–13% overstate multi-year skill, because many one-year winners are lucky and revert.
- "Profitable" is not "making a living": in Brazil only about 0.5% beat a bank teller's wage. A small-account trader who is genuinely skilled may still earn too little in absolute rupees to replace a salary.

### Gaps
- Could not fetch the original Barber et al. PDFs (faculty.haas.berkeley.edu blocked) to extract year-by-year profitable shares (for example the commonly quoted "about 80% lose in a typical year" or "fewer than 1% profitable 5 years running"). These are omitted rather than quoted unverified.
- No Indian academic panel study (multi-year persistence of individual F&O traders) was found. SEBI publishes only cross-sectional annual or multi-year aggregates.
- Barber, Lee, Liu & Odean (2009, RFS), "Just How Much Do Individual Investors Lose by Trading?", was not retrieved.

## 3. What characterises the profitable minority

### Takeaway
The persistent winners are mostly institutions using algorithms to provide liquidity or run arbitrage: prop desks, FPIs, HFTs and market makers. Among individuals, profitability is associated with trading less, not more. A tiny tail of skilled individual day traders exists, but their edge is small per day and depends on discipline and costs.

### Cited Findings
- In India, 96–97% of prop and FPI F&O profits in FY24 came from algo trading. Only about 13% of individuals used algos (overstated). — [BusinessToday](https://www.businesstoday.in/markets/story/93-of-individual-traders-incurred-losses-in-equity-fo-during-fy22-fy24-sebi-study-447102-2024-09-23)
- Trading frequency: 80% of very frequent intraday traders (more than 500 trades a year) lost money, against 71% overall, and loss-makers placed more trades than profit-makers. — [Business Standard](https://www.business-standard.com/amp/markets/news/7-in-10-intraday-traders-in-equity-cash-suffered-losses-in-fy23-sebi-study-124072400975_1.html)
- Age and experience: 76% of intraday traders under 30 were loss-makers, a higher share than other age groups. — [Business Standard](https://www.business-standard.com/amp/markets/news/7-in-10-intraday-traders-in-equity-cash-suffered-losses-in-fy23-sebi-study-124072400975_1.html)
- Instrument: about 92% of individuals' FY26 F&O losses came from options. — [Business Standard, Aug 2026](https://www.business-standard.com/markets/news/active-derivatives-traders-fall-18-in-fy26-to-8-75-million-sebi-study-126082001378_1.html)
- Costs: intraday loss-makers spent an extra 57% of their losses on trading costs. — [Business Standard](https://www.business-standard.com/amp/markets/news/over-70-intra-day-traders-incur-losses-during-fy23-reveals-sebi-study-124072401110_1.html)
- Infrastructure: co-located flow is a majority share of derivatives turnover (reported 62.1% in 2024). — [Investing.com India](https://in.investing.com/news/colocation-hits-357-algo-trading-surges-to-53-the-techdriven-shift-in-nse-4655643)
- Skill persistence: in Taiwan, prior-year top performers keep outperforming (37.9 bps/day after fees for the top 500). Skill exists but is concentrated in under 1% of traders. — [eScholarship](https://www.escholarship.org/uc/item/7k75v0qx)
- Scale of the best individual earnings: the best Brazilian persistent day trader made US$310/day with a US$2,560 daily standard deviation. — [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3423101)
- Capital and cross-market reach: Jane Street's gains came from running large positions in cash, futures and options at the same time, which needs a very large balance sheet. — [Mondaq](https://www.mondaq.com/india/commoditiesderivativesstock-exchanges/1648134/sebis-interim-order-against-jane-street-allegations-of-index-manipulation-explained)

### Inferences
- Strategy types that win structurally are **liquidity provision** (earning the bid-ask spread and exchange incentives, which needs speed and two-sided quoting), **arbitrage** (index/constituent, futures-cash, options parity, which needs low latency and big balance sheets) and **systematic risk premia** harvested with tight risk control. Directional option buying, the dominant retail activity, is the losing side on average.
- For a retail algo trader, the realistic edges are in lower-frequency systematic strategies where latency does not matter: multi-day trend or momentum, mean-reversion on daily bars, carefully hedged option selling with defined risk. Costs must be modelled explicitly, and fewer trades help because the SEBI frequency data and the Barber cost drag both punish high turnover.
- Discipline and risk management (small fixed-fractional risk, hard daily loss limits) separate survivors from blow-ups. Most losers do not have negative-edge ideas so much as cost drag plus oversized bets (see Section 4).

### Gaps
- No source retrieved directly documents the holding periods or order types (passive vs aggressive) of profitable individual traders in India. The Taiwan papers reportedly analyse liquidity provision by top traders, but this could not be verified without the PDFs.
- No SEBI breakdown of individual profitability by capital size was retrieved.

## 4. Position sizing, Kelly and risk of ruin: is "2% a day" survivable?

### Takeaway
Compounding 2% a day is about **141× a year**. Under standard Kelly mathematics, that growth rate needs a sustained annualised Sharpe ratio of about **3.2 even at full Kelly**, where the chance of the account halving at some point is about 50%. In practice, chasing a fixed daily target forces over-betting beyond Kelly, where expected log-growth turns negative and deep drawdowns become near-certain.

### Cited Findings
- **Kelly properties (idealised model with a known edge):**
  - A full-Kelly bettor has roughly a 1-in-2 chance that the account eventually halves. — [LuxAlgo](https://www.luxalgo.com/library/concept/kelly-criterion/)
  - A full-Kelly bettor has a **1/3 chance of halving the bankroll before doubling it**. A half-Kelly bettor has only a **1/9 chance**. These are different questions from "eventually halves", so they do not conflict. — [Albion Research](https://www.albionresearch.com/kelly/)
  - Half Kelly keeps about 75% of maximum expected growth with about half the volatility. Quarter Kelly keeps about 44%. — [Ryan O'Connell calculator](https://ryanoconnellfinance.com/calculators/kelly-criterion-calculator/); [FlashAlpha](https://flashalpha.com/concepts/kelly-criterion)
  - Ed Thorp advocated half Kelly or less in practice (secondary attribution). Real-world edges are usually overestimated, which is the main reason to use fractional Kelly. — [FlashAlpha](https://flashalpha.com/concepts/kelly-criterion)

### Inferences (my calculations; formulas stated so the writer can reproduce them)
- **Compounding:** 1.02^250 ≈ **141×** (1.02^252 ≈ 147×). 1%/day gives about 12× a year and 0.5%/day about 3.5×. For comparison, Medallion's reported 39% net a year is about **0.13%/day** geometric, and the Taiwan top-500 day traders' 37.9 bps/day after fees is about 2.6× a year if fully compounded on constant capital, which overstates real capacity.
- **Loss asymmetry** (gain needed to recover = L/(1−L)): a 10% loss needs 11.1%, 20% needs 25%, 30% needs 42.9%, 40% needs 66.7%, **50% needs 100%**, 60% needs 150%, 75% needs 300% and 90% needs 900%.
- **Sharpe needed for 2%/day (continuous-time Kelly):** maximum log-growth is S²/2 a year at full Kelly and 0.375·S² at half Kelly. 2%/day geometric is ln(1.02)×252 ≈ 4.99 a year in log terms. That needs **S ≥ 3.16 at full Kelly** and **S ≥ 3.65 at half Kelly**, sustained, net of all costs, with Gaussian returns. Fat tails make it worse. Sustained Sharpe ratios above 3 are typical only of HFT and market-making books with capacity limits, not retail directional strategies.
- **Drawdown probabilities under fractional Kelly c** (continuous model, P(ever falling to fraction x of starting wealth) = x^(2/c − 1)):
  - Full Kelly: P(ever −50%) = 50% and P(ever −80%) = 20%.
  - Half Kelly: P(ever −50%) = 12.5% and P(ever −80%) = 0.8%.
  - Quarter Kelly: P(ever −50%) ≈ 0.8%.
- **Worked binary example:** a strategy wins 55% of 1:1 trades with one trade a day, so Kelly f* = p − q = 10% of capital per trade.
  - To have an **arithmetic** expectation of 2%/day it must stake **20% per trade (2× Kelly)**. Expected log-growth is then 0.55·ln1.2 + 0.45·ln0.8 ≈ **−0.00014 per trade (negative)**, so the median outcome after 250 trades is about 0.97× (formula) or 0.79× (simulation), even though the edge is real.
  - Monte Carlo (20,000 paths, 250 trades):

    | Stake per trade | Kelly multiple | Median end wealth | P(drawdown from peak ≥50%) | P(end below 0.5×) | P(losing year) |
    |---|---|---|---|---|---|
    | 2.5% | ¼ Kelly | 1.77× | 1% | 0.1% | 8% |
    | 5% | ½ Kelly | 2.69× | 35% | 2% | 13% |
    | 10% | full Kelly | 3.16× | 97% | 10% | 23% |
    | 20% | 2× Kelly, the "2%/day" stake | 0.79× | 100% | 40% | 51% |

    (Mean wealth at 20% stakes is inflated by a few lucky paths, about 185×, which is how a few "2%/day" success stories coexist with most accounts being wiped out.)
- **Losing streaks:** with a 45% loss rate, the probability of at least one run of 6 straight losses in 250 trades is about 69%, 8 losses about 20% and 10 losses about 4%. Ten straight losses cost 9.6% of the account at 1% risk per trade, 18.3% at 2%, 40.1% at 5% and 65.1% at 10%.
- **Implication for small accounts:** a ₹1–5 lakh account aiming for 2%/day (₹2,000–10,000 a day) must either have an edge that no studied population of retail traders has shown (the top 500 Taiwanese earned about 0.38%/day, roughly a fifth of 2%), or use leverage of several times Kelly, which is mathematically a ruin strategy. Practitioners usually risk 0.5–2% of equity per trade and cap daily losses. A realistic skilled-retail target is closer to tens of percent a year than to percent a day.

### Gaps
- No primary Thorp/MacLean–Ziemba text was retrieved. The Kelly drawdown formula x^(2/c−1) and the S²/2 growth result are standard continuous-time results, presented here as my derivation and not quoted from a fetched source.
- No Indian data on the leverage or position sizes of losing vs profitable retail traders was found.

## 5. Behavioural and methodological pitfalls: what algos fix and what they don't

### Takeaway
Algos remove emotional execution errors such as hesitation, revenge trading, moving stops and over-trading after losses. They do not fix the bigger killers of systematic retail strategies: backtest overfitting and data-snooping, regime change, and decay of published or crowded edges. Academic anomalies lose about 58% of their returns after publication, and testing even a few dozen variants on a few years of data can manufacture a fake edge.

### Cited Findings
- **McLean & Pontiff, "Does Academic Research Destroy Stock Return Predictability?", *Journal of Finance*, 2016.** Across 97 published return predictors, portfolio returns are **26% lower out-of-sample** (an upper-bound estimate of data-mining effects) and **58% lower post-publication**, implying about 32 percentage points of decay from investors trading on the publication. Post-publication declines are larger for predictors with higher in-sample returns. — [Paper PDF (gwern mirror)](https://www.gwern.net/doc/economics/2016-mclean.pdf); [Ivey working paper](https://ivey.uwo.ca/media/3775549/pontiff.pdf)
- **Bailey, Borwein, López de Prado & Zhu, "Pseudo-Mathematics and Financial Charlatanism: The Effects of Backtest Overfitting on Out-of-Sample Performance", *Notices of the AMS*, May 2014.** A relatively small number of trials can produce a strategy with spuriously high backtested performance. The authors derive a **Minimum Backtest Length (MinBTL)** required for a given number of trials. — [AMS Notices PDF](https://www.ams.org/notices/201405/rnoti-p458.pdf)
- A follow-up by Bailey summarises the result as: with 5 years of daily data, **no more than about 45 strategy variations** should be tried, or the selected strategy is likely overfit. This is a secondary summary not checked against the original. — [Bailey et al., "Statistical Overfitting and Backtest Performance"](https://sdm.lbl.gov/oapapers/ssrn-id2507040-bailey.pdf)
- **Probability of Backtest Overfitting (PBO)** is the probability that the in-sample optimal strategy underperforms out-of-sample, estimated by combinatorially symmetric cross-validation (CSCV). — [Bailey, Borwein, López de Prado & Zhu, "The Probability of Backtest Overfitting"](https://www.davidhbailey.com/dhbpapers/backtest-prob.pdf); [SSRN](https://doi.org/10.2139/ssrn.2326253)
- **Deflated Sharpe Ratio:** the expected maximum Sharpe ratio across independently tested strategies grows with about √(log N) even when the true Sharpe is zero. The DSR corrects for this selection bias. — [summary in arXiv 2608.23808](https://arxiv.org/pdf/2608.23808); [Bailey online overfitting tools](https://www.davidhbailey.com/dhbpapers/overfit-tools.pdf)
- **Behavioural persistence:** in Taiwan, 74% of day-trading volume came from traders with a history of losses, consistent with overconfidence and biased self-assessment. — [EconPapers](https://econpapers.repec.org/article/ouprasset/v_3a10_3ay_3a2020_3ai_3a1_3ap_3a61-93..htm)
- **No learning:** Brazilian day traders showed no improvement with experience. — [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3423101)
- **Regime and regulatory change in India:** SEBI's 2024–25 measures cut individual participation (active traders down about 18% in FY26) and changed expiry-day dynamics. The Jane Street order shows that an expiry-day pattern can be declared manipulative after the fact. — [Business Standard, Aug 2026](https://www.business-standard.com/markets/news/active-derivatives-traders-fall-18-in-fy26-to-8-75-million-sebi-study-126082001378_1.html); [Business Standard on Jane Street](https://www.business-standard.com/markets/news/sebi-bars-jane-street-orders-rs-4844-cr-disgorgement-market-manipulation-125070400081_1.html)

### Inferences
- **What algos fix:** emotional execution, slippage from slow manual entry, missed stops, fatigue, inconsistent sizing, and over-trading after losses, provided the code enforces limits.
- **What algos don't fix:** (a) overfitting from parameter searches and indicator mining, (b) look-ahead and survivorship bias in data, (c) optimistic cost and slippage assumptions (decisive in Indian F&O, where costs add 57% to intraday losers' losses), (d) regime shifts such as volatility, expiry-calendar and lot-size changes, (e) edge decay from crowding (McLean & Pontiff's 58%), (f) operational risks such as API failures, runaway loops and fat-finger orders, and (g) the human tendency to override or abandon the system after drawdowns.
- **Rule of thumb for the writer:** haircut any backtested Sharpe or return by at least 50% (consistent with the 26–58% decay literature), and treat a backtest Sharpe above 2–3 on retail-accessible data as a likely sign of overfitting or errors.

### Gaps
- Harvey, Liu & Zhu (2016, RFS), "…and the Cross-Section of Expected Returns" (recommending t-statistics above 3.0), was not retrieved and is not cited.
- No India-specific study of retail algo or backtest decay was found.

## 6. Realistic benchmarks and how "2% a day" is marketed (SEBI actions)

### Takeaway
The best-documented trading operation in history, Renaissance's Medallion fund, reportedly averaged about 39% a year after fees (about 66% gross). Good Indian PMS strategies report about 15–25% CAGR. "2% a day" (about 14,000% a year compounded) is more than 100 times Medallion's net. SEBI repeatedly acts against those who market such returns, including the ₹546 crore Avadhut Sathe order (final, October 2026) and the 2022 ban on brokers and algo platforms advertising algo returns.

### Cited Findings
- **Medallion (1988–2018):** reported average annual returns of **66.1% before fees and 39.1% after fees**, from Zuckerman's 2019 book *The Man Who Solved the Market*. These are reported estimates for a private fund, not audited public series, and the figures are arithmetic averages. Bradford Cornell's reconstruction gives about 63.3% compound gross, with $100 in 1988 growing to about $398.7m by 2018. — [Quantt](https://www.quantt.co.uk/resources/medallion-fund-history); [Institutional Investor](https://www.institutionalinvestor.com/article/2bswymr8cih3jeaslxc00/portfolio/famed-medallion-fund-stretches-explanation-to-the-limit-professor-claims); [arXiv 2405.10917](https://arxiv.org/pdf/2405.10917v2)
- **Indian PMS benchmarks:** Buoyant Capital PMS reports a 15.42% 3-year and 18.07% 5-year return against 12.09% and 10.91% for the BSE 500 TRI. — [Kalviro Ventures analysis](https://www.kalviroventures.com/buoyant-capital-pms-vs-aif/)
- One PMS manager cites about 18–25% as the range for top-quartile PMS. — [Aequitas](https://www.aequitasindia.in/more/pms-returns-india/)
- League tables are inconsistent, with some implausible entries (for example a "123.69" 3-year figure), so the official per-strategy data from APMI should be used. — [AltPort](https://www.altportfunds.com/best-portfolio-management-services-pms/); [APMI performance data](https://www.apmiindia.org/apmi/welcomeiaperformance.htm?action=PMSmenu)
- **Persistent skilled day traders (Taiwan top 500):** 37.9 bps/day after fees. — [eScholarship](https://www.escholarship.org/uc/item/7k75v0qx)
- **SEBI circular of 2 Sep 2022:** stockbrokers offering algo services may not refer to the past or expected future performance of an algorithm, or associate with platforms that do. Brokers had 7 days to remove such references and disassociate. SEBI's concern was unregulated platforms marketing algos with claims of high returns. — [SCC Online](https://www.scconline.com/blog/post/2022/09/03/securitesandexchangeboardofindai-circular-performance-returnclaimed-unregulatedplatforms-offering-algorithimstrategies-trading-sebi-legal-updates-research-news/); [Business Standard](https://www.business-standard.com/article/markets/sebi-issues-guidelines-for-brokers-providing-algorithmic-trading-services-122090201262_1.html); [Moneylife](https://www.moneylife.in/article/sebi-warns-brokers-to-refrain-from-misselling-algo-trading-strategy-or-services-using-inflated-claims/68248.html)
- **2025 relaxation:** risk-return claims are allowed only if verified by a SEBI-recognised Past Risk and Return Verification Agency (PaRRVA). A PaRRVA must be a credit rating agency at least 15 years old with ₹100 crore minimum net worth. — [Medianama](https://www.medianama.com/2025/04/223-sebi-parrva-guidelines-updates-algo-trading-rules/)
- **Avadhut Sathe Trading Academy:**
  - SEBI's interim order of 4 Dec 2025 impounded about ₹546 crore and barred Sathe and the academy, finding unregistered investment advice "in the garb of stock market education". — [LiveLaw](https://www.livelaw.in/corporate-law/sebi-cracks-down-on-finfluencer-avadhut-sathe-impounds-546-crore-for-providing-unregistered-investment-advice-312335); [Business Standard](https://www.business-standard.com/amp/markets/news/avadhut-sathe-finfluencer-sebi-ban-disgorgement-unregistered-advisory-125120500178_1.html)
  - The academy gave stock-specific calls with entry, exit and stop-loss levels in live sessions and WhatsApp groups. It publicised profitable trades even though participants had net losses. — [Business Standard, Oct 2026](https://www.business-standard.com/markets/news/sebi-orders-avadhut-sathe-trading-academy-and-its-founder-to-refund-546-cr-126102301645_1.html); [LiveLaw Biz](https://www.livelawbiz.com/securities-law/sebi/securities-and-exchange-board-of-india-orders-avadhut-sathe-trading-academy-refund-546-crore-investors-imposes-11-crore-penalty-555837)
  - The **final order (Oct 2026)** directs a refund of ₹546.17 crore plus ₹67.87 crore interest, imposes ₹11.5 crore in penalties, and bars the academy and Sathe for two years or until the refund is made. — same sources; [BusinessToday](https://businesstoday.in/markets/story/who-is-avadhut-sathe-the-trader-behind-the-academy-at-the-centre-of-sebis-rs546-crore-order-563724-2026-10-26)
- SEBI has publicly advised investors not to engage with financial influencers (June 2024). — [News on AIR](https://www.newsonair.gov.in/sebi-advices-not-to-engage-with-financial-influencers)
- Later finfluencer rules, as reported by a secondary blog: a ban on registered entities associating with unregistered finfluencers, a 29 Jan 2025 circular restricting use of live market data in "education", and an Oct 2024 carve-out for SEBI-approved platforms. These were not verified against primary circulars. — [Dealplexus](https://www.dealplexus.com/blog/sebi-finfluencer-rules)

### Inferences
- Benchmarks for the writer:
  - Index (Nifty/BSE 500 TRI): about 11–12% a year over recent 3–5 year windows.
  - Good Indian PMS: about 15–25% a year.
  - The best quant fund ever: about 39% net (66% gross).
  - Top 0.1–1% of persistent day traders: about 0.4%/day on small capital, with severe capacity limits.
  - A skilled small-account retail algo trader who survives might plausibly target **15–40% a year with drawdowns of 15–30%**. Even that would put them in the top few percent of participants. This is my synthesis, not a measured statistic.
- The common marketing playbook ("2% daily", screenshots of winning days, courses that double as tip services, "fully automated" algo subscriptions) is exactly what SEBI's 2022 algo-claims ban, the PaRRVA regime and the Sathe order target. Highlighting winning trades while clients lose overall was an explicit finding in the Sathe case.

### Gaps
- No audited Indian quant-specific PMS/AIF league table was found. The APMI data must be filtered by hand.
- Prop-desk return norms in India (for example return on capital for NSE prop/HFT firms) were not found in public sources.
- Other finfluencer orders (for example the October 2023 "Baap of Chart" order and Asmita Patel in January 2025) were not retrieved, so their figures are not cited.

## 7. Best practices for developing a retail algo in India (testing, deployment, kill switches, regulatory framework)

### Takeaway
Treat any backtest as a hypothesis. Limit and record the number of variants tried, validate on untouched out-of-sample and walk-forward data, haircut the results heavily, paper-trade, then deploy live at tiny size behind hard risk limits and kill switches. In India, since SEBI's 4 Feb 2025 circular (live from about Aug–Oct 2025), retail API algos must also go through the broker as principal, carry an exchange-issued algo ID, and be registered above an orders-per-second threshold.

### Cited Findings
- **SEBI circular SEBI/HO/MIRSD/MIRSD-PoD/P/CIR/2025/0000013 (4 Feb 2025), "Safer participation of retail investors in algorithmic trading":**
  - Brokers act as principals and algo providers as their agents. Brokers need exchange permission for each algo they offer, handle grievances, and monitor APIs.
  - Every API algo order must carry an exchange-provided unique identifier, and changes to approved algos need exchange approval.
  - Algo providers must be empanelled with exchanges. Providers of "black-box" algos need a SEBI Research Analyst registration.
  - Retail investors' self-built algos must be registered through the broker once they exceed a specified orders-per-second threshold, and may be used by immediate family.
  - Exchanges keep a kill switch to disable orders from a specific algo ID.
  - [SEBI circular PDF](https://www.sebi.gov.in/sebi_data/attachdocs/feb-2025/1738665456458.pdf); [IndiaLaw summary](https://www.indialaw.in/blog/civil/sebi-retail-investors-algorithmic-trading/); [Marketfeed](https://www.marketfeed.com/read/en/an-overview-on-sebis-new-rules-on-algo-trading-for-retail-investors)
- NSE issued a retail-algo rulebook mandating strategy registration, effective 1 Aug 2025. — [Business Standard](https://www.business-standard.com/markets/news/nse-unveils-guidelines-for-retail-algo-trading-effective-august-1-125072301458_1.html); [Upstox](https://upstox.com/news/business-news/latest-updates/sebi-opens-doors-for-retail-investors-in-algo-trading-with-new-regulatory-framework/article-144719/)
- A kill switch is described as an emergency function and the last line of defence against algorithm malfunction, ideally triggering automatically on pre-defined conditions. — [CS Kruti guide](https://cskruti.com/sebis-2025-algo-trading-framework-a-practical-guide/)
- Business Standard advises algo users to understand the risks and keep realistic return expectations. — [Business Standard (Dec 2024)](https://www.business-standard.com/finance/personal-finance/algo-trading-understand-risks-have-realistic-return-expectations-124122001145_1.html)
- **Overfitting controls:** use MinBTL to choose a backtest length that supports the number of trials, PBO estimated with CSCV, and the Deflated Sharpe Ratio to correct for multiple testing. — [AMS Notices](https://www.ams.org/notices/201405/rnoti-p458.pdf); [Bailey et al. PBO](https://www.davidhbailey.com/dhbpapers/backtest-prob.pdf)
- **Decay:** expect out-of-sample returns about 26% lower than in-sample, and about 58% lower once an idea is public. — [McLean & Pontiff](https://www.gwern.net/doc/economics/2016-mclean.pdf)

### Inferences (recommended pipeline, synthesised from the sources above)
1. **Hypothesis first:** an economic reason for the edge (who is on the other side and why), not just indicator mining.
2. **Clean data:** survivorship-free, corporate-action adjusted, with realistic Indian costs (STT, exchange fees, stamp duty, GST, brokerage, slippage, impact on illiquid strikes) and lot-size and expiry-calendar changes.
3. **Limit and log trials:** keep the number of variants small relative to data length (MinBTL; about 45 variants for 5 years of daily data per Bailey's summary), and report the Deflated Sharpe and PBO.
4. **Walk-forward and out-of-sample:** rolling re-optimisation on past windows with testing on the next unseen window, plus a final hold-out period touched once. Test across regimes, for example the 2020 crash and the post-Nov-2024 expiry rules.
5. **Haircut** backtest returns by 50% or more before deciding on size.
6. **Paper or forward test** live for weeks to months to check fills, latency and API behaviour against the backtest.
7. **Small live deployment:** start at a fraction of intended capital and size at no more than ¼–½ Kelly on a haircut edge. Practically that means risking 0.25–1% of equity per trade.
8. **Hard controls in code and at the broker:** maximum loss per trade, per day and per week (for example stop trading for the day at −2–3%), maximum position and order size, order-rate throttles below SEBI's registration threshold unless registered, a manual and automatic kill switch, a heartbeat or disconnect handler that flattens or freezes positions, and alerts.
9. **Monitor for decay:** compare live against expected distributions (drawdown, win rate, slippage), and pre-define retirement criteria, for example a live drawdown beyond 1.5–2× the worst backtest drawdown.
10. **Compliance:** use broker-approved APIs with exchange algo IDs. Do not sell or share strategies or claim returns without the relevant SEBI registration (RA/IA) and PaRRVA verification.

### Gaps
- The exact SEBI orders-per-second threshold for mandatory retail algo registration, and the final post-extension go-live date, were not confirmed from primary sources. The Feb 2025 circular PDF could not be fetched.
- Practitioner references (Ernest Chan's books, López de Prado's *Advances in Financial Machine Learning*, Zerodha Varsity modules) were not retrieved directly. The pipeline above is a synthesis and not a quotation from them.
