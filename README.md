# Why-Microsoft-Should-Tap-into-Its-Gaming-IP-to-Open- a-Profitable-Movie-Studio

Our repository uses exploratory data analysis in order to determine how to create a profitable movie studio for Microsoft by maximizing Return on Investment (ROI).

# Findings

1. Precedent for successful video game movies.
2. Gaming genres align with top profitable genres.
3. Films at least two hours long tend to perform better.
4. Higher ratings lead to larger profits.
5. Profitable movies have greater global appeal.

# Data Analysis

We utilized the following datasets:

tn.movie_budgets.csv.gz
im.db
tmdb.movies.csv.gz
rt.reviews.tsv.gz
rt.movie_info.tsv.gz
bom.movie_gross.csv.gz

These datasets were provided by our course and we utilized these to determine which data we wanted to use as part of our analysis. After considering our approach for analysis, we selected the imdb database as well as The Number's movie budgets csv in order to gain a better understanding of the production budget, domestic and worldwide gross of the movies, and number of votes for each movie used in our dataset.

We filtered for production budgets of over 10m dollars, runtimes of 75min or more, and movies with at least 1000+ ratings in order to gain a representative number of votes.

# Notebooks

Preliminary data exploration was done in ancillary notebooks, utilizing names of our members in order to differentiate between each other. Information regarding how we arrived at our master data set, as well as final findings have been pulled from those notebooks into the **final_notebook**. The other notebooks have been moved to a subfolder called notebooks.

# final_notebook

The first major block of the final_notebook describes the initial import and connection to database to understand the data that was worked with. After merging the files of interest together to create an initial data frame.

The data frame then added an additional column calculating the ROI for the movies analyzed.

Data frame was further filtered in order to select movies that had a production budget greater than 10M, movie runtime of over 75min, and number of review votes that were greater than 1000.

### Precedent for successful video game movies

When the data frame was cross referenced against a list of video game movies that were released during the same time frame, the high ROI demonstrates success in this genre of movies.

### Gaming genres align with top profitable genres

### Films of at least two hours tend to perform better

### Higher ratings lead to higher profits

### Profitable movies have greater global appeal


## Presentation is available as [PDF](https://github.com/albertcchen/dsc-phase-1-project/blob/main/presentation.pdf)