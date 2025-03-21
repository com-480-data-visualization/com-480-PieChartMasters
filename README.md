# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
|Jérôme Baras | 326256 |
|Marc Bonhôte Tomasini | 325411 |
|Eliot Goncalves | 330553 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 1 (21st March, 5pm)

**10% of the final grade**

This is a preliminary milestone to let you set up goals for your final project and assess the feasibility of your ideas.
Please, fill the following sections about your project.

*(max. 2000 characters per section)*

### Dataset

We chose multiple datasets to capture both micro-level (mortgage lending) and macro-level (unemployment, global indicators) dimensions of the 2008 financial crisis. By combining data from the CFPB, FRED, World Bank, and others, we aim to highlight how individual borrower behavior and institutional practices intersected with broader market forces, culminating in a historic economic downturn.


**1. Economic and Market Data in the USA**  
- **[US Real Estate Prices (FRED – ASPUS)](https://fred.stlouisfed.org/series/ASPUS)**  
  - **Usage**: Compare real estate prices before and after the crisis.  
- **[Unemployment Rate (FRED – UNRATE)](https://fred.stlouisfed.org/series/UNRATE)**  
  - **Usage**: Track unemployment as a key social impact.  
- **[Wealth of the Poorest Households (FRED – WFRBLB50107)](https://fred.stlouisfed.org/series/WFRBLB50107)**  
  - **Usage**: Assess the crisis’s impact on the most vulnerable groups.
- **[State-Level Debt-to-Income ratio (Federal Reserve)](https://www.federalreserve.gov/releases/z1/dataviz/household_debt/state/map/#year:2008)**

**2. Financial Institutions & Banking Sector**  
- **[Banks Acquired/Bankrupted (Wikipedia)](https://en.wikipedia.org/wiki/List_of_banks_acquired_or_bankrupted_during_the_Great_Recession?utm_source=chatgpt.com)**  
  - **Usage**: Map affected institutions (location, losses, etc.).  
- **[Subprime Crisis Writedowns (Wikipedia)](https://en.wikipedia.org/wiki/List_of_writedowns_due_to_subprime_crisis)**  
  - **Usage**: Show MBS/CDO losses by institution or region.  
- **[FDIC Failed Bank List](https://www.fdic.gov/bank-failures/failed-bank-list)**  
  - **Usage**: Analyze official bank failures (dates, assets, acquiring institutions) to understand spatial and temporal patterns.

**3. Global Data & Confidence Indicators**  
- **[OECD Consumer Confidence Index](https://www.oecd.org/fr/data/indicators/consumer-confidence-index-cci.html?oecdcontrol-b2a0dbca4d-var3=2005-05&oecdcontrol-b2a0dbca4d-var4=2012-02)**  
  - **Usage**: Map worldwide consumer confidence in relation to the crisis.  
- **[World Bank – World Development Indicators (WDI)](https://data.worldbank.org/indicator)**  
  - **Usage**: Evaluate global crisis impact (GDP, debt, unemployment, healthcare).

**4. US Mortgage Sector**  
- **[Comprehensive Mortgage Data (HMDA, CFPB)](https://www.consumerfinance.gov/data-research/hmda/historic-data/?geo=nationwide&records=all-records&field_descriptions=labels)**  
  - **Features**: Loan type, amount, demographics, location; links defaults to socio-economic indicators.  
  - **Usage**: A valuable dataset for understanding the characteristics of mortgage lending before the collapse, providing insights into the factors that contributed to the crisis.  
- **[Mortgages 90+ Days Delinquent (CFPB)](https://www.consumerfinance.gov/data-research/mortgage-performance-trends/mortgages-90-or-more-days-delinquent/)**  
  - **Usage**: Identify delinquency clusters on a map over time. This dataset provides actual performance data, enabling clearer spatio-temporal insights into mortgage defaults.

**5. Stock Market & Sentiment Analysis**  
- **[Financial Market Data (Yahoo)](https://finance.yahoo.com/)**  
  - **Usage**: Retrieve historical indices (S&P 500, Dow, NASDAQ), visualize crash and recovery, compare sector performance.  
- **[Google Trends](https://trends.google.fr/trends?geo=CH&hl=fr)**  
  - **Usage**: Study searches for “mortgage”, “subprime”, "crisis" etc.; identify interest peaks; gauge public sentiment.


### Problematic

The general topic of our visualization is about the 2008 subprime mortgage crisis. The main goal is to understand the evolution of the crisis geographically and temporally.

Here is an overview of the different aspect of the crisis that we want to show through some visualizations in order to understand them :

**1. Understand the dynamics of mortgage defaults:**
- With an interactive map of the United State, we want to highlight how mortgage defaults spreads over time in order to identify regional clusters of high default rates.
- On the same visualization, we could also shows whether defaults started in specific locations.
- By adding other economic factors (such as real estate price, unemployment, and other factors), we can highlight possible correlations on another visualization. 

**2. Understand the international and socioeconomic impact of mortgage defaults:**
- With an interactive map of the world, we want to highlight how the crisis spread in the world through various economic indicators (Consumer index, ...) and see which country were most affected by the financial crisis.
- With time-series graphs of various socioeconomic indicators (like unemployement, net worth, household debt, ...), we want to highlight how household wealth eroded post-crisis.

**3. Understand the effects on financial markets:**
- With a time series of major stock indices supplemented with crisis events marked in order to understand the timeline of the crisis and how the financial market reacted in response to key events.
- With a Bubble map of companies loss and companies that goes in bankruptcy, we want to highlight to major financial institutions that collapsed.
   
**4. Identify the early warning signals and their spread:**
- With a heatmap or a word cloud using Google Trends, we want to highlight how economic fear propagated.
- Completting this with a timeseries to understand when the fear started to propagate

The visualizations above will help us understand the subprime mortgage crisis, revealing the key indicators, how they changed over time, and the underlying reasons behind the meltdown. Highlighting patterns and trends, this analysis not only explains the past, but attempts to identify possible early signals providing a framework that could be applied to predict and avoid future financial crises.

### Exploratory Data Analysis

> Pre-processing of the data set you chose
> - Show some basic statistics and get insights about the data

For our chosen subject, many relevant datasets, such as US real estate prices (FRED – ASPUS), unemployment rate (FRED – UNRATE), and OECD consumer confidence index, are readily available from reputable sources like the Federal Reserve (FRED), OECD, and the World Bank. These datasets are typically clean, pre-processed single-feature time series that clearly illustrate the crisis's impact, often showing a distinct drop or spike around 2008.   

While we will use HDMA data from 2007–2010 in practice, we will here explore the 2007 dataset since it is representative of the aggregate. This dataset includes 953,569 mortgage applications and 78 features covering loan details, borrower demographics (population, genre), and lending decisions. Key categorical variables include loan type, loan purpose, property type, and applicant credit factors, while numerical features such as loan amounts, income, and approval rates provide insights on the lending characteristics leading up to the crisis and assess how borrower characteristics influenced loan approval and potential defaults. After preprocessing, more than 20 features were dropped due to excessive missing values or irrelevance.

The dataset reveals significant disparities in loan amounts and applicant incomes. Loan amounts range from $1,000 to nearly $100M (median: $140K; mean: $182K), while incomes span from $1K to almost $10M (median: $69K; mean: $95.6K). Loans are geographically diverse, covering 16,075 ZIP codes across 1,711 counties in all 50 states. Refinancing is the primary loan purpose (~47%), followed by home purchases (~40%) and home improvements (~8%).


### Related work

Multiples institutions and researchers have used the HMDA dataset for similar analyses: 

- Urban Institute & Housing Finance Policy Center: Analyzed mortgage denial rates, small-dollar lending, and racial disparities in lending.
(https://apps.urban.org/features/mortgages-by-race/)
- Federal Reserve & CFPB: Regularly published reports on mortgage market trends using HMDA data.
- Journalists & Data Scientists: Used HMDA data to map the mortgage crisis, focusing on regional default rates and their impact on minority communities (https://jhucovid19.policymap.com/blog/using-hmda-data-to-understand-lending-activity-in-detroit)
- Academic Studies: Researchers have built models to analyze how mortgage defaults propagated through the banking system. While the exact datasets may vary slightly, they contain similar types of financial information.

Our approach is still original because most project done on these dataset were focused on specific aspects like the race : https://apps.urban.org/features/mortgages-by-race/. In our project, leveraging the use of differents datasets, we want to to include multiples perspectives like the international economic impact, the impact on the quality of life, on institutional collapses and analyze the fear of the crisis. All these elements will be integrated into dynamic visualizations, to provide and interactive and broad understanding of the subject.

We have some nice inspiration like the url displayed above even if it is lacking of interactivity, we would like to pursue and deepen the usage they made of the map.
We also looked at project of students of these last years and the project on the formula 1 history(https://formula1viz.altervista.org/index.html) is very well realized and it would also be interesting to have an interactive map linked with displayed graphs / statistics.

## Milestone 2 (18th April, 5pm)

**10% of the final grade**


## Milestone 3 (30th May, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

