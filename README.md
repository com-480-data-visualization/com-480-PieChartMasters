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
1. Données Économiques et de Marché aux USA
- Prix de l’immobilier aux USA
    - Source : FRED – ASPUS
    - Utilisation : Visualiser l’évolution des prix immobiliers avant et après la crise.
    - Idée visuelle : Animation « bubble burst » pour illustrer la forte baisse des prix.

- Évolution du taux de chômage aux USA
    - Source : FRED – UNRATE
    - Utilisation : Suivre l’évolution du chômage, indicateur clé de l’impact social de la crise.

- Patrimoine des ménages les plus modestes
    - Source : FRED – WFRBLB50107
    - Utilisation : Mesurer l’impact de la crise sur la richesse des plus fragiles économiquement.

2. Données sur les Institutions Financières et le Secteur Bancaire
- Liste des banques acquises ou en faillite durant la Grande Récession
    - Source : Wikipedia – List of banks acquired or bankrupted during the Great Recession
    - Utilisation : Créer une carte des institutions financières affectées (localisation, montant des pertes, etc.).

- Liste des pertes (writedowns) dues à la crise subprime
    - Source : Wikipedia – List of writedowns due to subprime crisis
    - Utilisation : Visualiser l’ampleur des pertes sur certains produits financiers (MBS, CDO) par institution ou région.

3. Données Globales et Indicateurs de Confiance
- Indice de confiance des consommateurs
    - Source : OECD Consumer Confidence Index (CCI)
    - Utilisation : Cartographier l’évolution de la confiance des consommateurs à l’échelle mondiale, en lien avec l’impact de la crise.
5. Données sur le Secteur Hypothécaire aux USA
- Données complètes sur les prêts hypothécaires (HMDA)
    - Source : Consumer Finance – Historic HMDA Data
    - Caractéristiques : Comprend des informations sur le type de prêt, montant, caractéristiques démographiques (race, sexe, revenus), localisation (état, comté, tract, etc.). Permet d’analyser la répartition des défauts de paiement et de faire des liens avec d’autres indicateurs socio-économiques.
      - Utilisation : Création de cartes dynamiques des défauts aux USA, analyses statistiques croisées (salaire, situation de crédit, taux de défaut).

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

