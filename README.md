# IMDB

# Business Problem
What makes a successful movie? Can we use publicly-available data from past movies to predict the success of future
ones? To make recommendations to increase the success of future movies?

# Tasks
1. Generate a MySQL database on Movies from a subset of IMDB's publicly available dataset
2. Analyze Movie data for trends
3. Main Question: What makes a successful movie?
4. Generate a model to predict movie success

# Data Sources:
- The data used for this project will be obtained from [IMDB](https://www.imdb.com/interfaces/) and 
[TMDB](https://www.themoviedb.org/about?language=en-US)
- IMDB has several publicly-available datasets, from these the client selected three with relevant information:
    - [Basics](https://datasets.imdbws.com/title.basics.tsv.gz)- 
    As the name implies, basic information about the movies in the dataset
    - [Ratings](https://datasets.imdbws.com/title.ratings.tsv.gz)-
    Contains the IMDb rating and votes information for titles 
    - [AKAs](https://datasets.imdbws.com/title.akas.tsv.gz)-
    more information about the titles
- Other pertinent information will be queried from TMDBs public database using
 [their API](https://www.themoviedb.org/documentation/api?language=en-US)
 
# Data Collection and Storing
## Cleaning IMDB Data
The publicly-available data from IMDB contains many movies not relevant to this study. 
Only those movies fitting the specifications provided by the client will be included.
The specifications and procedure may be found in [IMDB_Cleaning](imdb_cleaning.ipynb)

## TMDB Querying and EDA
- TMDB API was queried using [tmdb_query.ipynb](tmdb_query.ipynb)
- The Following visualizations were made during some basic EDA

<img src='img/financial_eda.png' width=200>
<img src='img/num_movies_certification.png' width=200>
<img src='img/ave_bud_by_cert.png' width=200>
<img src='img/ave_rev_by_cert.png' width=200>
<img src='img/ave_profit_by_cert.png' width=200>


## Creating a MySQL Database
<img src='img/imdb_erd.png'>

# Data Analysis
## Clustering and Feature-Engineering
## Exploratory Analysis
## Hypothesis Testing
### Does the MPAA rating of a movie (G/PG/PG-13/R) affect how much revenue the movie generates?
Because the P-value is less than 0.05 we reject the null hypothesis and accept that MPAA rating affects the revenue of the movie
### Do movies that are over 2.5 hours long earn more revenue than movies that are 1.5 hours long (or less)?
Yes, because the p-value is less than 0.05 we can reject the null hypothesis and accept that revenue is greater for movies longer than 150 minutes than for movies shorter than 90 minutes.
### Do movies released in 2020 earn less revenue than movies released in 2018?
Yes, the p-value is less than 0.05 so we can reject the null hypothesis and accept the alternative that movies in 2020 earned less in revenue than movies in 2018.

# Predictive Model
# Recomendations





