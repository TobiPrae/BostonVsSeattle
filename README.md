# BostonVsSeattle

Hi, welcome to my project. I created this repository for the first project I had to do during my data science nano degree on udacity. Here is a short summary of the project (for more details I refer to the Jupyter notebook).

Business Understanding:
I analyzed Airbnb listings from Seattle and Boston. I aimed to answer the following questions:
  1. How do the cities differ in price?
  2. Which factors had a particularly strong influence on the price?
  3. Are there certain areas in the cities that cause Airbnb accommodation prices to go up?

Data Understanding:

I had 3 data sets available for each city: Listings, Reviews and Calendar. I decided to use only the first one.         Since I didn't want to do a text analysis, I didn't use Reviews. I didn't find the information from Calendar too    interesting, especially because the prices column didn't contain any values. Listings on the other hand contained a lot of information like amenities, zip codes, prices and reviews. 

For listings, I first looked at all the columns and looked at their NaN proportions as well as what values they could each take. Based on that I selected a few columns manually as columns_of_interest. These include review-related columns, price, zip code and amenities.

Prepare Data:
During the preparation steps, I removed mainly NaN entries. Since I checked before that my selected columns do not have too many NaN entries, I did not lose too much information. I didn't want to impute any values because I didn't want to distort the analysis. I also had to create dummy variables for non-numeric columns and parse the price column from string to float.

Data Modeling:

How do the cities differ in price?
- For this purpose, I mainly used the measures mean and median. Since both are standard indices for numerical values. The mean is susceptible to outliers, which is why I also took the median.
- As a visualization I chose the box plot because it can display a lot of information in a very compact way.
- In addition, I have chosen a barplot to visualize the average prices per ZIP code
  
Which factors had a particularly strong influence on the price?
- First, I want to build a first multivariate linear regression model and calculate RMSE and R2-score. 
- Secound, I want to perform a correlation analysis. For this I use the build in correlation function of pandas and I use the default figure, the Pearson Correlation Coefficient (PCC)
- Based on this analysis I want to keep all features that have a PCC of >0.1 or <-0.1 and drop the rest
- Then I want to train another LM to see wether the measures improved or not
- To visualize my results I choose to plot the featers that correlated the most with price (positively and negatively)

Are there certain areas in the cities that cause Airbnb accommodation prices to go up?
- To answer this, I wanted to plot the prices and the zip-price-correlation on a geomap using geopandas

Evaluation:
- Boston seems to be more expensive than Boston, this indicates the median as well as the mean
- Features like the number of beds and bedrooms seemed to lead to higher prices, the number of review, however, seems to correlate negatively with the price
- Especially listings that were in the city center had a higher zip-price-correlation

The following files are in the repository:
- lol

To execute my code you need the modules:
- pandas
- numpy
- math
- re
- geopandas
- matplotlib
- sklearn



The medium blog post can be found here: https://tobias-praetori91.medium.com/airbnb-listings-in-boston-and-seattle-how-do-they-differ-d98e8f49623f
