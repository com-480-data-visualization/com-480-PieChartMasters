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

- US Real Estate Prices
  
        - Source: FRED – ASPUS
        - Usage: Visualize the evolution of real estate prices before and after the crisis.
        - Visual Idea: “Bubble burst” animation to illustrate the significant drop in prices.
  
- Evolution of the Unemployment Rate in the USA
  
        - Source: FRED – UNRATE
        - Usage: Track the evolution of unemployment, a key indicator of the social impact of the crisis.
  
- Wealth of the Poorest Households
        - Source: FRED – WFRBLB50107
        - Usage: Measure the crisis’s impact on the wealth of the most economically vulnerable groups.
  
**2. Data on Financial Institutions and the Banking Sector**

- List of Banks Acquired or Bankrupted During the Great Recession
        - Source: Wikipedia – List of banks acquired or bankrupted during the Great Recession
        - Usage: Create a map of the affected financial institutions (location, amount of losses, etc.).
- List of Writedowns Due to the Subprime Crisis
        - Source: Wikipedia – List of writedowns due to subprime crisis
        - Usage: Visualize the magnitude of losses on certain financial products (MBS, CDO) by institution or region.
- FDIC Failed Bank List
        - Source: FDIC Failed Bank List
        - Usage: Deepen the analysis of bank failures in the United States with official information (closing dates, assets, acquiring institutions) to understand the spatial and temporal distribution of failures during the crisis.
  
**3. Global Data and Confidence Indicators**

- Consumer Confidence Index
        - Source: OECD Consumer Confidence Index (CCI)
        - Usage: Map the evolution of consumer confidence worldwide, in connection with the impact of the crisis.
- World Bank – World Development Indicators (WDI)
        - Source: World Bank – WDI
        - Usage: Analyze various global indicators (GDP, debt, unemployment rate, and effects on other sectors such as healthcare) to assess the scope of the financial crisis worldwide and its sectoral repercussions.
  
**4. Data on the US Mortgage Sector**

- Comprehensive Mortgage Data (HMDA)
        - Source: Consumer Finance – Historic HMDA Data
        - Features: Includes information on loan type, amount, demographic characteristics (race, gender, income), location (state, county, tract, etc.). Enables analysis of the distribution of payment defaults and correlation with other socio-economic indicators.
        - Usage: Creation of dynamic maps of defaults in the USA, cross statistical analyses (salary, credit situation, default rate).
  
**5. Additional Data: Stock Market Indicators & Sentiment Analysis**

- Financial Market Data (Yahoo Finance / Google Finance)
        - Source: Yahoo Finance or Google Finance
        - Usage:
            - Retrieve historical data on stock indices (S&P 500, Dow Jones, NASDAQ, etc.), bank stock prices, bond yields.
            - Visualize the market crash during the crisis and the subsequent recovery.
            - Compare the financial sector’s performance with other sectors of the economy.
- Google Trends for Sentiment Analysis
        - Source: Google Trends
        - Usage:
            - Study the evolution of searches related to terms such as “mortgage,” “subprime,” or “financial crisis.”
            - Identify peaks in public interest and correlate them with key crisis events.
            - Adopt a qualitative approach to understand consumer perception and concerns.

### Problematic

> Frame the general topic of your visualization and the main axis that you want to develop.
> - What am I trying to show with my visualization?
> - Think of an overview for the project, your motivation, and the target audience.

The general topic of our visualization is about the 2008 subprime mortgage crisis. The main goal is to understand the evolution of the crisis geographically and temporally.

Here is an overview of the different aspect of the crisis that we want to show through some visualizations in order to understand them :
1. Understand the dynamics of mortgage defaults:
    - With an interactive map of the United State, we want to highlight how mortgage defaults spreads over time in order to identify regional clusters of high default rates.
    - On the same visualization, we could also shows whether defaults started in specific locations.
    - By adding other economic factors (such as real estate price, unemployment, and other factors), we can highlight possible correlations on another visualization. 

2. Understand the international and socioeconomic impact of mortgage defaults:
    - With an interactive map of the world, we want to highlight how the crisis spread in the world through various economic indicators (Consumer index, ...) and see which country were most affected by the financial crisis.
    - With time-series graphs of various socioeconomic indicators (like unemployement, net worth, household debt, ...), we want to highlight how household wealth eroded post-crisis.

3. Understand the effects on financial markets:
    - With a time series of major stock indices supplemented with crisis events marked in order to understand the timeline of the crisis and how the financial market reacted in response to key events.
    - With a Bubble map of companies loss and companies that goes in bankruptcy, we want to highlight to major financial institutions that collapsed.
   
4. Identify the early warning signals and their spread:
    - With a heatmap or a word cloud using Google Trends, we want to highlight how economic fear propagated.
    - Completting this with a timeseries to understand when the fear started to propagate

The visualizations above will help us understand the subprime mortgage crisis, revealing the key indicators, how they changed over time, and the underlying reasons behind the meltdown. Highlighting patterns and trends, this analysis not only explains the past, but attempts to identify possible early signals providing a framework that could be applied to predict and avoid future financial crises.

### Exploratory Data Analysis

> Pre-processing of the data set you chose
> - Show some basic statistics and get insights about the data

**Exploratory Data Analysis – Pre-processing Overview**

For most of the selected datasets—such as real estate prices (FRED), unemployment data (FRED), consumer confidence (OECD), and global indicators (World Bank)—the data is already well-structured and cleaned. These sources typically provide consistent, aggregated, and standardized information with minimal missing values or anomalies. As a result, only minimal preprocessing (e.g., basic checks for date alignment or outlier detection) is required for these datasets.

However, the mortgage dataset (HMDA) is substantially larger and noisier, containing multiple columns, various categorical features, and some missing or incomplete records. This dataset will require more extensive data cleaning and preprocessing steps, such as:
- Handling missing values in key fields (e.g., applicant income, property location).
- Standardizing categorical variables (loan type, race, ethnicity, etc.) to ensure consistency.
- Removing or imputing outliers and invalid entries (e.g., negative or zero loan amounts, duplicated rows).

By focusing additional effort on the mortgage dataset’s preprocessing, we can ensure that the rest of the datasets—already in good shape—will integrate smoothly for subsequent analyses and visualizations.

### Related work


> - What others have already done with the data?
> - Why is your approach original?
> - What source of inspiration do you take? Visualizations that you found on other websites or magazines (might be unrelated to your data).
> - In case you are using a dataset that you have already explored in another context (ML or ADA course, semester project...), you are required to share the report of that work to outline the differences with the submission for this class.

## Milestone 2 (18th April, 5pm)

**10% of the final grade**


## Milestone 3 (30th May, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

