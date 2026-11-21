# Analytics Portfolio | Julian Devonish

Eight analytics projects combining HTML/SVG and Tableau dashboards, including Jamaican credit and lending intelligence.

**Start with the live dashboard** and its Data & Methodology or Start Here view. Use the case studies to understand decisions, measures and limitations. Download the HTML/SVG source bundle or Tableau workbook to inspect the implementation.

**[Back to my profile](https://github.com/Jdevonish25)** · **[All live dashboards](https://public.tableau.com/app/profile/jul.dev/vizzes)** · **[Machine learning capstone](https://github.com/Jdevonish25/Capstone_FMA_Project)**

## Jamaica Credit Intelligence

[Open dashboard](https://jamaica-credit-intelligence-julian.sparklingcocoa64.chatgpt.site) · [Technical case study](Jamaica-Credit-Intelligence-case-study.md) · [HTML/SVG source and data](Jamaica-Credit-Intelligence-source.zip)

**Decision context:** understand lending growth, sector exposure and the distribution of overdue balances in Jamaica’s deposit-taking system.

**Data:** 115 monthly observations from Bank of Jamaica, March 2017–September 2026, retrieved 21 November 2026. Published lending, loan-quality and business-size tables; no synthetic financial observations.

**Experience:** four views combine executive KPIs, linked sector selection, an exposure-growth scatterplot, loan-quality trends, a monthly heatmap and documented calculations. The HTML/CSS/SVG interface includes reporting-month controls, tooltips and downloadable data.

**Skills:** Python ingestion, wide-to-long transformation, financial ratio definitions, reconciliation, custom SVG visualization, responsive UI design and analytical communication.

**Interpretation:** month-end balances are stocks, not new loan issuance. Sector classifications differ between lending and arrears tables, so no unverified sector default rates are constructed. This is a sourced snapshot and descriptive analysis, not a risk prediction model.

## NBA Courtside — The Modern Era

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/NBACourtside-TheModernEra/01Courtside) · [Download workbook](NBA%20Courtside%20-%20The%20Modern%20Era.twbx) · [Technical case study](NBA-Courtside-case-study.md) · [Build scripts](NBA-Courtside-source.zip)

**Analytical question:** how do player production, team efficiency and league playing style vary across seasons, and how can viewers compare them without mixing counting units?

**Data and preparation:** NBA.com Stats observations via Larry's public nba_data mirror, covering 2014–15 through 2026–27, through 20 November 2026. Regular season and playoffs remain separate. The extract has 9,546 player records, 582 team records and 25 league aggregates, with each worksheet restricted to its appropriate grain. Player point totals reconcile to team totals in every season/competition combination.

**Experience:** five pages cover the league overview, player matchups, team identity, era trends and a viewer guide. The opening **Starting Five** uses embedded NBA player portraits that change with the selected season, competition and category (points, rebounds, assists or threes per game). Its rank filters match the leaderboard, with names and rates displayed beside the photographs.

**Skills demonstrated:** Python ingestion and preparation, source provenance, multi-grain modeling, KPI denominator control, Tableau parameters, calculated fields, embedded custom shapes, interactive ranking, data storytelling and source reconciliation.

**Interpretation:** the 2026–27 season is partial; the publication is a static snapshot. The exploratory leader pool requires at least five appearances and 15 minutes per game, not official NBA qualification. Ties use unrounded rates then alphabetical names. Traded players retain season totals and their last team label. Latest NBA portraits do not imply historical team affiliation. No NBA endorsement; descriptive comparisons do not establish causes.

**Attribution:** [NBA.com Stats](https://www.nba.com/stats), [nba_data mirror and documentation](https://github.com/llimllib/nba_data). Portraits: NBA.com. Source hashes and image credits accompany the technical case study.

## Jamaica Tourism Demand

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/Jamaica-TourismDemandIntelligence_17951847615340/01DemandBrief) · [Download workbook](Jamaica%20-%20Tourism%20Demand%20Intelligence.twbx)

**Decision context:** identify changes in tourism demand, seasonal exposure and dependence on source markets to inform market prioritization and planning.

**Data and preparation:** Jamaica Tourist Board monthly source-market workbooks for 2023–2025. Published subtotal rows were excluded, monthly columns were unpivoted, and detailed arrival counts were reconciled to the published annual and monthly controls. The analytical table contains 11,160 rows.

**Analysis:** year-over-year arrival changes, source-market contribution, monthly seasonality and market concentration. The prepared 2025 snapshot totals 2,601,416 arrivals versus 2,900,358 in 2024, a decrease of approximately 10.3%. The United States contributes about 70.7% of 2025 arrivals, highlighting concentration to investigate alongside changes in other markets.

**Skills demonstrated:** data restructuring, reconciliation, period comparisons, segmentation and executive dashboard design.

**Interpretation:** counts are arrival events, not unique people, bookings or hotel nights; cruise arrivals are excluded. Published reporting areas mix countries, U.S. states, Canadian provinces and residual categories. These are historical snapshots subject to revisions. The dashboard does not establish causes, revenue effects or hotel occupancy.

## Jamaica Financial Access

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/Jamaica-ExecutiveIntelligence/01ExecutiveBrief) · [Download workbook](Jamaica%20-%20Executive%20Intelligence.twbx)

**Decision context:** understand financial access, inclusion gaps and digital readiness in Jamaica, with regional comparisons and economic context.

**Data and preparation:** publicly available World Bank indicator series, including Global Findex account ownership, IMF financial access measures and internet-use indicators. The underlying data also includes inflation, remittances, GDP per capita and unemployment. Each observation retains its indicator, geography and year so that unlike periods are not presented as a single survey.

**Analysis:** account ownership by gender and income group, branch and ATM availability, digital access and selected economic signals. Comparisons support questions about access barriers and the feasibility of digital channels rather than assuming that account ownership equals regular use.

**Skills demonstrated:** multi-source indicator modeling, metadata documentation, comparative analysis and communication of time-period differences.

**Interpretation:** indicators have different release cycles and latest observation years. Ownership does not prove active usage, digital literacy or service quality. Associations are descriptive and do not establish causation. The workbook is a sourced snapshot rather than a live feed.

**Attribution:** [World Bank indicator catalog](https://data.worldbank.org/indicator) and [Global Findex](https://www.worldbank.org/en/publication/globalfindex). World Bank data licensing and the originating agencies' terms apply.

## IslandPay Payments

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/IslandPay-Publish_17950382440110/IslandPayPaymentsPulse) · [Download workbook](IslandPay%20-%20Publish.twbx)

**Decision context:** monitor payment volumes, successful payment value and reliability; identify channels and failure categories that warrant operational investigation.

**Data and creation:** 88,601 fictional Jamaican payment attempts spanning January–June 2026, generated in Python for this portfolio using a fixed random seed. The scenario includes payment channels, merchant categories, amounts and outcomes, with designed patterns for comparative analysis. IslandPay is a fictional portfolio scenario; this is not a company's operational dataset and contains no real customer records.

**Analysis:** volume and value trends, successful attempts divided by all attempts, channel comparisons and failure patterns. The full snapshot contains 84,593 successful attempts, approximately 95.48% success, and about JMD 391.0 million in successful value. Wallet filtering produces 44,246 attempts and approximately 97.01% success.

**Skills demonstrated:** synthetic data preparation, precise KPI denominators, filter validation, diagnostic comparisons and responsive executive reporting.

**Interpretation:** patterns are simulated. Neither the payment values nor changes are evidence of actual revenue, customer behavior or business impact. Suggested operational actions are examples of how an analyst could use comparable real data.

## CreditLens

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/CreditLens-DigitalLendingCreditRisk/01PortfolioBrief) · [Download workbook](CreditLens%20-%20Digital%20Lending%20%26%20Credit%20Risk.twbx)

**Decision context:** examine observed default patterns and repayment behavior to identify segments for further credit-risk investigation.

**Data and preparation:** 30,000 Taiwan credit-card client records from April–September 2005, with a next-month default label, from UCI's *Default of Credit Card Clients*. Monthly records were unpivoted, explicit bands were derived and a fixed 100-account sample supports detailed exploration. Currency is New Taiwan dollars (NTD), not Jamaican dollars.

**Analysis:** 6,636 clients have the observed next-month default label, a 22.12% rate in this historical sample. In the derived September two-or-more-month delay group, 2,177 of 3,130 clients have that label, about 69.55%. The comparison illustrates a strong historical association to investigate rather than a causal effect.

**Skills demonstrated:** account-versus-month grain management, cohort segmentation, denominator control, repayment-history analysis and risk communication.

**Interpretation:** this is descriptive historical credit-card analysis, not a Jamaica lending dataset, loan approval system or validated predictive scorecard. No fair-lending, current-market or production deployment claim is made.

**Attribution:** I-Cheng Yeh, [UCI dataset](https://archive.ics.uci.edu/dataset/350/default), [DOI 10.24432/C55S3H](https://doi.org/10.24432/C55S3H), CC BY 4.0. Adaptations include renamed fields, unpivoted monthly history and derived analytical bands.

## FDA Product Recalls

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/FDAProductRecallData/FDAProductRecall) · [Download workbook](FDA%20Product%20Recall%20Data.twbx)

**Decision context:** explore how product-recall records vary by hazard classification, geography and archived status to support further review of recall patterns.

**Data and implementation:** an archived U.S. FDA product-recall dataset packaged with the workbook. Views present product-record counts, standard hazard classes and archived statuses. The historical snapshot is labeled so that a viewer can distinguish it from a current safety feed.

**Skills demonstrated:** categorical and geographic comparisons, clear counting units and dashboard explanations that prevent overinterpretation.

**Interpretation:** a product record is not necessarily a separate recall event. Record counts do not measure affected consumers, recall severity by volume, manufacturer quality or current product safety. Review original FDA notices before making safety decisions. Source fields and snapshot context can be inspected in the workbook; this project does not claim a refreshed FDA feed.

## Superstore Performance

[Open dashboard](https://public.tableau.com/app/profile/jul.dev/viz/SampleSuperstore_16854554175570/SalesDashboard) · [Download workbook](Sample%20Superstore.twbx)

**Decision context:** compare sales and profit across regions, states and product categories to identify commercial performance differences and areas for deeper margin analysis.

**Data and implementation:** Tableau Sample Superstore demonstration data. The full dataset represents approximately USD 2.30 million in sales, USD 286,397 in profit and **5,009 distinct orders**. Orders use `COUNTD(Order ID)` so multiple product lines in one order are not counted as separate orders. The state map represents total profit in USD.

**Analysis:** monthly trends, regional and product comparisons, and geographic profit distribution. These support questions about revenue contribution versus profitability without equating either measure with order count.

**Skills demonstrated:** distinct-count measures, aggregation checks, commercial KPI interpretation and appropriate use of bars, trends and maps.

**Interpretation:** this is a sample retail dataset for demonstration. It does not describe a real employer's results or substantiate realized savings or revenue growth.

## Quality and responsible interpretation

- Every workbook includes a viewer guide covering purpose, sources, counting unit, metric definitions, filters and limitations.
- Published snapshots were checked for layout and calculation behavior; original embedded Hyper extracts were preserved during the portfolio presentation review.
- Reported snapshot figures describe these datasets. They are not claims of business results achieved for an employer.
- Professional experience is summarized on the profile. Employer datasets, internal dashboards and confidential deliverables are not included here.
- Workbooks contain embedded extracts. To view interactively without Tableau Desktop, use the live dashboard links above. A `.twbx` download can be opened in a compatible Tableau application.

## Contact

[LinkedIn](https://www.linkedin.com/in/julian-devonish-588b3732b/) · [jdevonish25@gmail.com](mailto:jdevonish25@gmail.com)
