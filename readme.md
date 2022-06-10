I. Risk Assessing Integrated Analysis Dashboard

- Multiple data sources
- Alternative Assets
- Asset Valuation
- Portfolios
- Loss Forecasting
- Statistical Metrics

Risk Analysis

- vehicle asset
- lending period
- default risk
- loan seasoning
- discounting factor for bundling

Business Intelligence

- Visualizations
- A/B Testing
- Behavioral grouping
- "Impressions" or similar volume

Systems Integration

- API datafeed ingestion
- Data quality checks
- exploratory data analysis
- data pipelines
- data transformation
- database schemas

Quantitative Analysis

- portfolio creation
- short-term versus long-term assets
- "drivers" based separation
- value at risk and expected exposure
- risk-factor identification and modeling

II. Ideas and Connections

<hr>

A. Debt Instrument - Loan Portfolio
- connection to the stock prices of he vehices involved
- there is also credit exposure here. borrowers have credit scores.
- how much can you as a bank lose on defaulting loans, and still make money?
  - limit losses by liminting the default rate
  - charge enough of an interest rate
  - these are NOT unsecured loands. The asset it part of the recovery rate.
- FICO score
- Internal scoring method
   - loan purpose
   - job length
   - monthly income
   - bank savings
- A settlement or a payment plan helps the reovery rate evem after going from deliquency into default
- https://www.youtube.com/watch?v=JfpfNESluyM
- How do write-offs or charge-offs work?
  - is that actually lost money?
- Should you be making or losing money for servicing it?
- Is there a place where you can see what the secondary market is for selling a bundle of your loans?
- "Portfolio-At-Risk" measurement
  - e.g. PAR 30 is the percenage of outstanding loan balance that is 30 days or more overdue
  - can this be simulated?
  - http://support.loandisk.com/support/solutions/articles/17000016657-portfolio-at-risk-par-
- There will be some correlation between the stocks for the vehicle companies, and the assets involved in the other major parts BIZ-INTEL, UZR/HOSPITALITY, FIN MRKT INDICES
  - how is this supposed to be take into account?
  - does it increase or decrease some sort of risk?
  - how can the defaulr risk of YOUR firm itself be asessed?
  - if you have a defualt risk, then this would be applied to your CVA for other types of financing you might enter into 

<hr>

B. Dashboarding and Analytics
- Evergreen, industry-less, industry-agnotic metrics about our first set of data: the vehicle assets
- Three addressed-dimension graphs, that use size, color, and or position to add additional dimensionf of comparison to a 2D plot
- seaborn, or plotly or matplotlib
- what are the best types of monochrome or grey-scale (max 4 shades) graphs?
- FUNNEL?
  - is there a customer funnel we can elaborate on, such as the path to vehicle purchase over a certain time, and cross-sectionally?
  - can we simulate some sort of A/B test?
    - what would A and B, be?
    - what uplift would we be trying to show/prove?
  - display - impression - views - click - homepage - item page - add to cart - abandon cart - order - sale
  - acqusition cost
  - ratio of any two (adjacent) items in the path, and it's reciprocal if meaningful
- Can we A/B test strategies in our portfolio?
  - how woud you replicae the idea of "users" only being in one group or the other?
  - Maybe a blind split of all securities of the market A1/B1 versus a definitive split based on
    - strategy
    - criteria
    - market, price, or value driver
- Is there a "simple segments" behaviors (vs user-identified) concept we can incorporate?
  - Visitor, Browser, Customer, Abandon Cart ??

