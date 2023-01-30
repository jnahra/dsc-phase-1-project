# Why Microsoft Should Tap Into Its Gaming IP to Open a Profitable Movie Studio

Our repository uses exploratory data analysis in order to determine how to create a profitable movie studio for Microsoft by maximizing Return on Investment (ROI).

# Findings

1. Precedent for successful video game movies.
2. Gaming genres align with top profitable genres.
3. Films at least two hours long tend to perform better.
4. Higher ratings lead to larger profits.
5. Profitable movies have greater global appeal.

# Data Analysis

We utilized the following datasets:

- tn.movie_budgets.csv.gz
- im.db
- tmdb.movies.csv.gz
- rt.reviews.tsv.gz
- rt.movie_info.tsv.gz
- bom.movie_gross.csv.gz

These datasets were provided by our course and we utilized these to determine which data we wanted to use as part of our analysis. After considering our approach for analysis, we selected the IMDb database as well as The Number's movie budgets csv in order to gain a better understanding of the production budget, domestic and worldwide gross of the movies, runtimes, genres and ratings for each movie used in our dataset.

We filtered for production budgets of over $10 million, runtimes of 75 minutes or more, and movies with at least 1000+ ratings in order to gain a representative number of votes.

# Notebooks

Preliminary data exploration was done in ancillary notebooks, utilizing names of our members in order to differentiate between each other. Information regarding how we arrived at our master data set, as well as final findings have been pulled from those notebooks into the **final_notebook**. The other notebooks have been moved to a subfolder called notebooks.

# final_notebook

The first major block of the final_notebook describes the initial import and connection to database to understand the data that was worked with. We merged the files of interest together to create an initial data frame.

We added a new column that calculated ROI for the movies in our dataset.

Data frame was further filtered in order to select movies that had a production budget greater than $10 million, movie runtime of over 75 minutes, and number of review votes that were greater than 1000.

### Precedent for successful video game movies

The data frame was cross referenced against a list of video game movies that were released during the same time frame. These movies exhibited solid ROI, dmonstrating the potential for success for other video game movies.

![Video Game Movies vs. ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/videogame_movies_roi.png)

### Gaming genres align with top profitable genres

For genre, a weighted mean ROI measure was used, which gives more weight to films with larger budgets and revenue. This was felt to be appropriate given the potential for smaller sample sizes when grouping by genre. To mitigate these small sample sizes somewhat, only genres with more than five movies were used.

![Top_10_Genres_by_Weighted_ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Top10_Genre_Weighted_ROI.jpeg)

### Films of at least two hours tend to perform better

Next, the runtime data was analyzed against mean ROI in order to determine if any trends could be established between run time and ROI. This data was grouped into bins of 15 minute increments and it was determined films of at least two hours appear to have a higher ROI.

![Mean_ROI_vs_Runtime](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Mean_ROI_Runtime.jpeg)

### Higher ratings lead to higher profits

We charted mean ROI for different rating bins (ratings are measured out of 10). ROI increases dramatically as ratings rise past 6 out of 10.  Unsurprising but a reminder that film quality matters.

![Mean_ROI_vs_Rating](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Mean_ROI_Rating.jpeg)

### Profitable movies have greater global appeal

Analysis was performed for the most profitable and the most unprofitable movies. It was determined that the difference between the two was their domestic revenue share. More profitable movies tended to have a lower domestic revenue share, indiciating that more of their revenue came from international sources.

![Top100_by_ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/top100_byROI.png)

## Conclusion

Based on the analysis performed, we recommend making video game movies, which align with current successful movie genres. At least two hours appears to be the optimal runtime to achieve the highest possible ROI. Higher rated films performed better at the box office so quality of the film must be considered. Finally, appealing to international markets should be kept in mind to maximize ROI.

## Presentation is available as [PDF](https://github.com/albertcchen/dsc-phase-1-project/blob/main/presentation.pdf)