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

> Find a dataset (or multiple) that you will explore. Assess the quality of the data it contains and how much preprocessing / data-cleaning it will require before tackling visualization. We recommend using a standard dataset as this course is not about scraping nor data processing.
>
> Hint: some good pointers for finding quality publicly available datasets ([Google dataset search](https://datasetsearch.research.google.com/), [Kaggle](https://www.kaggle.com/datasets), [OpenSwissData](https://opendata.swiss/en/), [SNAP](https://snap.stanford.edu/data/) and [FiveThirtyEight](https://data.fivethirtyeight.com/)), you could use also the DataSets proposed by the ENAC (see the Announcements section on Zulip).
>

**1. Economic and Market Data in the USA**  
- **US Real Estate Prices (FRED – ASPUS)**  
  - **Usage**: Compare real estate prices before and after the crisis.  
  - **Visual Idea**: “Bubble burst” animation.  
- **Unemployment Rate (FRED – UNRATE)**  
  - **Usage**: Track unemployment as a key social impact.  
- **Wealth of the Poorest Households (FRED – WFRBLB50107)**  
  - **Usage**: Assess the crisis’s impact on the most vulnerable groups.

**2. Financial Institutions & Banking Sector**  
- **Banks Acquired/Bankrupted (Wikipedia)**  
  - **Usage**: Map affected institutions (location, losses, etc.).  
- **Subprime Crisis Writedowns (Wikipedia)**  
  - **Usage**: Show MBS/CDO losses by institution or region.  
- **FDIC Failed Bank List**  
  - **Usage**: Analyze official bank failures (dates, assets, acquiring institutions) to understand spatial and temporal patterns.

**3. Global Data & Confidence Indicators**  
- **OECD Consumer Confidence Index**  
  - **Usage**: Map worldwide consumer confidence in relation to the crisis.  
- **World Bank – World Development Indicators (WDI)**  
  - **Usage**: Evaluate global crisis impact (GDP, debt, unemployment, healthcare).

**4. US Mortgage Sector**  
- **Comprehensive Mortgage Data (HMDA, CFPB)**  
  - **Features**: Loan type, amount, demographics, location; links defaults to socio-economic indicators.  
  - **Usage**: A valuable dataset for understanding the characteristics of mortgage lending before the collapse, providing insights into the factors that contributed to the crisis.  
- **Mortgages 90+ Days Delinquent (CFPB)**  
  - **Usage**: Identify delinquency clusters on a map over time. This dataset provides actual performance data, enabling clearer spatio-temporal insights into mortgage defaults.

**5. Stock Market & Sentiment Analysis**  
- **Financial Market Data (Yahoo/Google Finance)**  
  - **Usage**: Retrieve historical indices (S&P 500, Dow, NASDAQ), visualize crash and recovery, compare sector performance.  
- **Google Trends**  
  - **Usage**: Study searches for “mortgage,” “subprime,” etc.; identify interest peaks; gauge public sentiment.


### Problematic

> Frame the general topic of your visualization and the main axis that you want to develop.
> - What am I trying to show with my visualization?
> - Think of an overview for the project, your motivation, and the target audience.

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

**Exploratory Data Analysis – Pre-processing Overview**

Most of our selected datasets (e.g., real estate prices, unemployment, consumer confidence) are single-feature time series from reputable sources such as the Federal Reserve (FRED), OECD, and the World Bank. They typically display a notable drop or spike around 2008, reflecting the financial crisis’s impact. Because these datasets are already clean and straightforward, we will focus our exploratory analysis on the HMDA mortgage dataset, which is larger and requires more preprocessing.


### Related work


> - What others have already done with the data?
> - Why is your approach original?
> - What source of inspiration do you take? Visualizations that you found on other websites or magazines (might be unrelated to your data).
> - In case you are using a dataset that you have already explored in another context (ML or ADA course, semester project...), you are required to share the report of that work to outline the differences with the submission for this class.

Multiples institutions and researchers have used the HMDA dataset for similar analyses: 

- Urban Institute & Housing Finance Policy Center: Analyzed mortgage denial rates, small-dollar lending, and racial disparities in lending.
(https://apps.urban.org/features/mortgages-by-race/)
- Federal Reserve & CFPB: Regularly published reports on mortgage market trends using HMDA data.
- Journalists & Data Scientists: Used HMDA data to map the mortgage crisis, focusing on regional default rates and their impact on minority communities (https://jhucovid19.policymap.com/blog/using-hmda-data-to-understand-lending-activity-in-detroit)
- Academic Studies: Researchers have built models to analyze how mortgage defaults propagated through the banking system. While the exact datasets may vary slightly, they contain similar types of financial information.

Our approach is still original because most project done on these dataset were focused on specific aspects like the race : https://apps.urban.org/features/mortgages-by-race/. In our project we want to to include multiples perspectives like the international economic impact, the impact on the quality of life, the impact on institutional collapses and even the fear of crisis. All these elements will be integrated into dynamic visualizations, ensuring smooth and interactive storytelling.

We have some nice inspiration like the url displayed above even if it is lacking of interactivity, we would like to pursue and deepen the usage they made of the map.
We also looked at project of students of these last years and the project on the formula 1 history(https://formula1viz.altervista.org/index.html) is very well realized and it would also be interesting to have an interactive map linked with displayed graphs / statistics.

## Milestone 2 (18th April, 5pm)

**10% of the final grade**


## Milestone 3 (30th May, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

