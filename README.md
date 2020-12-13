# BostonVsSeattle

Hi, welcome to my project. I created this repository for the first project I had to do during my data science nano degree on udacity. 

The medium blog post can be found here: https://tobias-praetori91.medium.com/airbnb-listings-in-boston-and-seattle-how-do-they-differ-d98e8f49623f

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
  
  
    Question 2
        Analyze
        Visualize
        Brief explanation for visualization
    Question 3
        Analyze
        Visualize
        Brief explanation for visualization
Evaluation
    Findings





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
