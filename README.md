# Flatiron School Data Science Program: Module 2 Project

## Introduction

The purpose of the project was to build a multilinear regression model using an exisiting data set. While Netflix is far and away the most popular streaming platform used today, not much is known on how exactly Netflix analyzes their data and measure the performance of their content. That is why I chose to explore the data that is available to the public and analyze what could be used as measures of success for the Movie and Television content that is currently available for streaming on Netflix.

### Business Case
Other than tracking viewership, the average user ratings listed on the Internet Movie Database (IMDb) plays a significant role in content discover for Movies and TV shows. Audiences rely on these ratings and the rankings that come out of them as a reference for what would be the best content to watch and how popular it is. With that said , what particular features are involved in generating these ratings and how can they be used to predict ratings for future Netflix content?

### The Data
The main data set consists of Netflix titles and was downloaded from the following kaggle user: https://www.kaggle.com/shivamb/netflix-shows?select=netflix_titles.csv

Additionally, the IMDB user ratings for those titles was webscrapped by this kaggle user: https://www.kaggle.com/aalhendi/netflix-movies-and-tv-shows-ratings .
 .
To generate a list of the top grossing directors, the folling data set was used: https://www.kaggle.com/tmdb/tmdb-movie-metadata .

And lastly, API calls from The Movie Database (TMDb) was also used for this project to get the popularity rating for each TV show and movie.

### Methodologies
- Data Collection
- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Statistical Testing
- Model Development


### Findings

From my EDA and stats tests, there appeared to be a correlation between the average IMDb user rating and the popularity of the Netflix content. The popularity rating from TMDb is based on several different factors including the number of votes and views a Movie/TV Show page gets for the day, the number of useres who marked it as a "favorite", the release date, and other factors. However, this data is not entirely presentable as this can change day by day and since it calculates those metrics per day, the information collected is bias towards more recent Netflix content.

From the statistical tests,  there is not a significant relationship between IMDb ratings and the season the content was added to Netflix and also the relation between ratings and the maturity rating of the Netflix content.

The categories, maturity ratings, and the duration are measured differently between Netflix Movies and TV shows. In addition, after running a two sample t-test, it was found that there is significant difference in the average IMDb user ratings between Movies and TV shows on Netflix. Therefore, I chose to evaluate two separate models, one for Movies and one for TV shows.

##### Movies
- R-sqaured : 0.354
- Train RMSE: 0.728
- Test RMSE: 0.963
Number of reviews, Documentaries, Dramas, India, PG

##### TV Shows
- R-sqaured : 0.354
- Train RMSE: 0.747
- Test RMSE: 1.009
- Number of reviews, Kid’s TV, and Reality TV

For both my Movies data set and TV data set, I had a low R-squared meaning that the features that I had did not do much to explain the variance in either case.

My best model was through Lasso for both, and the RMSE are a little less than one standard deviation from the mean average IMDb User ratings for both.

Lastly the features with the strongest corrletions were the number of reviews for both, Documentaries, Dramas, India, and PG for Movies. And then the duration in seasons, Kid's TV, and Reality TV were the strongest for TV Shows.

In conclusion, I feel that my model is not quite where it should be and I would like to find more features to use in this. I would also like to explore the cast data and also utilize social media and google trend metrics with more time to build my model. I would also find it interesting to evaluate this model based on original Netflix content specifically to assess if Netflix really produces content with a similar quality as regular shows and movies released traditionally.

