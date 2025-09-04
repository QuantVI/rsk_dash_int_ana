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
  - ( Browsers, Customers, Shoppers, and Abandoned Cart.) is the official simple segmentation from back then.
- Could there be a behavioral component to the people we lend to?
  - for example, on-time payment for people in certain groups lead to forebearance periods, or slightly lowered premiums?
- Statistical significance of A/B tests
  - sample means comparison
  - sample variances comparison. ANOVA?
- Sales projection.
  - if X dollars created Y sales, then is there a non-linear way to predict what 2X or 3X dollars would lead to?
  - would this involve time-series, or just a function of all the funnel inputs/parameters?
- ARIMA forecast
- Contribution margin
- https://medium.com/geekculture/how-to-forecast-sales-with-advertising-spend-in-r-36e6fc99760a
- Look up causal models for sales projecion/prediciton

<hr>

C. Data Inegration, APIs, System Analysis, Databases, Data Pipelines, User-level Profiles
- What de we have at the User level?
- Is there a User? 
- Is it our consumer? Such as who we lend to
1. Can we create a User profile?
  - what would make the User profie "rich"?
  - the original concept
    - history of stays
    - promoter score (external)
    - internal survey score
    - sentiment analysis score
    - other preferences
    - Is this just demoraphic data?
      - https://www.yieldify.com/blog/types-of-market-segmentation/
      - demographic, psychographic, geographic, behavioral
    - also, show when their "NEXT STAY" is (maybe ike a prediction on what they will be and when
    - also shows a level, or loyalty to location and brand (maybe akin to a a portfolio weighted in certain industries and sub industries
      - how are industries broken down?
      - https://www.investopedia.com/terms/s/sector-breakdown.asp#:~:text=our%20editorial%20policies-,What%20Is%20a%20Sector%20Breakdown%3F,investment%20criteria%20and%20overall%20objective.
      - GICS Sector
      - https://www.investopedia.com/terms/g/gics.asp
      - https://eresearch.fidelity.com/eresearch/markets_sectors/sectors/sectors_in_market.jhtml
      - https://www.ilo.org/global/industries-and-sectors/lang--en/index.htm
2. APIs
  - here's where datafeeds come in
  - We have to use Yahoo Finance - but this is just a csv download endpoint (or a function call from a package)
  - What about Polish Stooq - but this is most likely just scraping
    - Is the Polish market useful for us?
    - Does it specialize in anything?
  - Then there's Inded, which ha sa true API.
    - The API endpoint exists. We would need to ake our own functionailty to interact with it
    - At the least, we'd need to understand the API calls and what they return to faciitate what we need
    - Indeed could be used for job-availability-proxy data, for potential borrowers
    - We could also hunt down employer reputations from here, e.g. rating score on a 5 point scale
    - We could also get sentiment form here and score it
  - Glassdoor
    - another potential locaton for employer ratings, sentiment, and job availability, e.g. soft local economy score
  - LinkedIn
    - In addition to jobs data, this oculd be a chance to do the "name association" thing
    - Name Association: What top 5 jobs do people with your name usually have?
      - that job can be ranked, and put into an estimate salary range using sites like this
      - the estimated salary can be a proxy for "luck in life", and be a favorable factor in lending
      - I think LinkedIn has an API
  - With a true API, scraping, and csv download, we've covered "integration"
  - However, we should integrated, or build to integrate to 2 true APIs at least
    - in  the first pass version, this can be skipped or done csv/extract style
  - This is a good place to make a database decision, and it combines with the Part-A "UACC" stuff.
    - should we stick with SQLite since it can be made on-the-fly and saved to disk?
    - Also with SQLite we don't need the SQL GU front-end, so no need for MySQL
    - Can Python made PostgreSQL compliant db files?
      - go chance to learn PostgreSQL variant. Does it have windowing functions?
    - ElasticSearch: How hard would t be to relate an ES-compliant database?
      - what would we be searching in the first place?
      - should the user profiles live here? It is JSON. Easy diwplay, and compatibility with a web front-end
      - How does Github render raw JSON?
  - We're going to need an object model and schema setup. 
    - What information should objects hold?
    - What are our main objects?
    - How should the detailed information be split?
    - Star-schema?
  - Can you push to database by making changes in the front-end?
  - Dataflow:
    - what is the order of operations for data entering the system?
    - Are the transformations?
    - Does ingestion + transformation = pipeline?
    - Which systems should be upstream or downstream?
    - **UNDO** ! There needs to be a way to back-out changes at various object and hierarchy levels.
    - In addition to an object model and a database schema, we need an ENTITY?? model.
      - our major systems or "services" will have names, and need to connect to each other in certain ways
      - uh oh don't microservice everything.
      - this requires a diagram
    - Ingestion: We probably need a data ingestion queuing system ,like RabbitMQ or something similar and much simpler
      - Does ingestion queue + ingestion order = data pipeline?
    - **Systems Analyst**
      - The system itself needs metrics, monitoring, data quality checks, and snapshots along the beginning to end of the flow of data

<hr>

D. Quantitative Risk Analysis and Management
  - Last (ignore the machine learning extras) but not least.
  - This is what we're trying to build for
  - Alpha, Beta, Smart Beta, Tracking Error, etc <-- when are these used in concert with one another?
    - clearly these are portfolio metrics, but for what type(s) or portfolio(s)?
    - When is portfolio management used instead of risk management?
    - When would we care about tracking error (Port Man), instead of vol VaR and ES (Risk Man)?
  - FRTB
    - what are your risk-factors and exposures?
    - How do you measure them?
    - How are they quantified?
    - Are you passing modellability and liquidity tests?
    - What are your trading versus banking? i.e. short-term vs holdings
  - You need a pricer.
    - Price vehicle assets based on???
    - Price equities, derivatives, etc.
      - what models will you use?
      - will you model all of your risk factors? volatility, rate, underlying, volume?
    - Sensitivity and Sensitivity Analysis
    - Scenario Analysis - essentially stress-testing

<hr>
**Extra**

1. Where can you incorporate Machine Leaning and Neural Networks into this?
1. Could a transformer model be explored and used here in anyway?
1. What about Fourier wave transformation for input data?
1. If there is a way to include this a multi-step prediction model would be best
- that is, when you run the prediction _once_ you get multiple time-steps ahead predicted
- alternatively, you feed in a series and get out a series (fixed length or otherwise)
