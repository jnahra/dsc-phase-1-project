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

![Video Game Movies vs. ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/videogame_movies_roi.png)

### Gaming genres align with top profitable genres

For genre, weighted mean ROI measure was used, which gives more weight to films with larger budgets and revenue. This was felt to be appropraite given the potential for smaller sample sizes when grouping by genre.

Only genres with more than five (5) movies in each genre were used in order to group these categories together. this allowed more weight to larger films using the weighted ROI rather than giving more weight to smaller films with high ROIs using mean ROI, since for this case analysis a large film budget would most likely be used.

![Top_10_Genres_by_Weighted_ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Top10_Genre_Weighted_ROI.jpeg)

### Films of at least two hours tend to perform better

Next, the runtime data was analyzed against mean ROI in order to determine if any trends could be established between run time and ROI returned. This data was grouped into bins of 15 minute increments and it was determined films of at least two (2) hours appear to have a higher ROI. Also interesting to note that the ROI of movies approaching three hours are also high ROI.

![Mean_ROI_vs_Runtime](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Mean_ROI_Runtime.jpeg)

### Higher ratings lead to higher profits

The next variable explored was if different ratings can help increase mean ROI. Ratings, measured out of ten (10), were grouped into bins and plotted against the mean ROI. It was determined that ratings greater than 6 yielded higher mean ROI than the other bins.

![Mean_ROI_vs_Rating](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/Mean_ROI_Rating.jpeg)

### Profitable movies have greater global appeal

Analysis was performed for the most profitable and the most unprofitable movies. It was determined that the difference between the two was their domestic revenue share. More profitable movies tended to have a lower domestic revenue share, indiciating that more of their revenue came from international sources.

![Top100_by_ROI](https://github.com/albertcchen/dsc-phase-1-project/blob/main/Graphs/top100_byROI.png)

## Based on the analysis performed, we recommend creating video game movies aligning with current successful movie genres. Movies of at least two hours length appear to be the optimal runtime to achieve the highest possible ROI. Higher rated films also performed better at the box office so quality of the film must also be considered. Finally, international markets should also be kept in mind for better performing films.

## Presentation is available as [PDF](https://github.com/albertcchen/dsc-phase-1-project/blob/main/presentation.pdf)