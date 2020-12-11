# BostonVsSeattle

Hi, welcome to my project. I created this repository for the first project I had to do during my data science nano degree on udacity. 

The medium blog post can be found here: https://tobias-praetori91.medium.com/airbnb-listings-in-boston-and-seattle-how-do-they-differ-d98e8f49623f

I analyzed Airbnb listings from Seattle and Boston. I aimed to answer the following questions:
1. How do the cities differ in price?
- I compared the cities by plotting the prices with a box plot
- In addition, I compared the mean prices by zip code
- My results of both analyses indicate that Boston ist more expensive

2. Which factors had a particularly strong influence on the price?
- To answer this I built a multivariate linear regression model and calculated RMSE and R2-Score
- The I used the corr() function of pandas and sorted the features by correlation with price
- I found out that for example the number of bed and bedrooms correlate positively with the price
- The number of reviews, however, correlated negatively
- I took all features that had a correlation coeefficient with >0.1 or < -0.1 and used them for a secound linear model
- The results were slightly worse. Therefore, further feature engineering could be helpful

3. Are there certain areas in the cities that cause Airbnb accommodation prices to go up?
- Since I found out that certain ZIP codes correlate negatively or positivley I added a column for each listing if its zip code correlatates posetively, negatively or not at all
- I then used geopandas to plot my results
- For both cities listings in the center seemed to have higher prices

To execute my code you need the modules:
- pandas
- numpy
- math
- re
- geopandas
- matplotlib
- sklearn
