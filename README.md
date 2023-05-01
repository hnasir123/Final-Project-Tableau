# Final-Project-Tableau

## Project/Goals - Airbnb Analysis of New York City
In this project, we will analyze a dataset of Airbnb listings in New York City to gain insights into the local market and explore the factors that affect pricing. By examining variables such as location, property type, reviews, and pricing, we hope to uncover patterns and trends that can help us understand the trends and behavior in the listings.

Using data visualization tools Tableau, we will create charts, graphs, and maps to help us explore the data and identify interesting patterns and relationships. We will also use statistical analysis techniques to draw meaningful conclusions from the data. Below are the questions we are trying to answer


1.	How has the number of Airbnb listings in each neighborhood changed over time?
2.	Are there any seasonal patterns in the listings
3.	Which neighborhoods have the highest number of Airbnb listings?
4.	What is the average price per night for Airbnb rentals in each neighborhood?
5.	What is the most common type of property and room listed on Airbnb?
6.	How does the price of Airbnb rentals vary based on the number of beds in the listing?
7.	What is the distribution of review scores ratings for Airbnb listings?
8.	What is the distribution of Price for Airbnb listings?
9.	Is there a relationship between the number of beds and the price of the listing?
10.	Is there a relationship between the review scores rating and the price of the listing?


## Process
## Step 1 – Connect the dataset with Tableau

First, I imported into Tableau  the Airbnb New York City listings dataset which is a CSV format

## Step 2 – Exploratory Analysis
Then I did the exploratory analysis of all the data and following are the observations
1.	Two fields, Review Scores Rating (bin) and Review Scores Rating, are there in the dataset and are almost the same in values (correlation about 1.0). It appears that these fields contain score rating of each of the properties and are collected using a different methods. The results are almost same we can use any of the fields for analysis.
2.	The Price data is skewed and contains some outliers like there are properties having price of 10000 and 8000. Since the average of price is 164 we can filter out the properties with price greater than 1000 
3.	 In Review Scores Rating some of the score are missing so we can filter these properties out while building visuals and will consider ratings that are not 0.

 I created a line chart that showed the number of listings over time. This allowed me to identify any trends or seasonal patterns in the data, and I found that there was a reduction in the number of listings in 2014.
Next I created a bar chart that showed the number of listings by neighborhood, which allowed me to identify the neighborhoods with the highest and lowest number of Airbnb listings.
I then created a bar chart that showed the number of listings by property type, which allowed me to identify the most popular property types.
Next, I created a bar chart that showed the number of listings by room type, which allowed me to identify the most popular room types among Airbnb hosts in New York City.
Next I created density plot to check for any relation between Price vs Rating and No. of Beds vs Price.


## Results
Below are the results and analysis method used for each questions

1.	How has the number of Airbnb listings in each neighborhood changed over time?
For this questions I created a time series line plot indicating the number of listing over time in years for each neighborhood and found that there was a increase in number of listings until Q2 of 2014 then there is decrease in trends of number of listings. On investigation I find that its due to the legal challenges faced by Airbnb in New York City during that time. In 2014, there was a major crackdown on illegal short-term rentals, which resulted in many Airbnb hosts facing fines and legal action. This led to a decline in the number of hosts who were willing to rent out their properties on Airbnb, which resulted in  reduction in the number of listings.
2.	Are there any seasonal patterns in the listings
For this questions I created a time series line plot for each month and find that during July and December seasons the number of listing increased due to vacation seasons
3.	Which neighborhoods have the highest number of Airbnb listings?
For this question I created bar chart for number of listings in each neighborhood and found that Manhattan has the highest number of listings
4.	What is the average price per night for Airbnb rentals in each neighborhood?
For this question I created  bar chart for number of listings in each neighborhood for price and found that Manhattan has the highest average price for rentals at 185$ and Brooklyn has average price of 125$
5.	What is the most common type of property and room listed on Airbnb?
Using bar chart we find that Apartments are the most listed property type with more than 27000 apartment listings
6.	How does the price of Airbnb rentals vary based on the number of beds in the listing and Is there a relationship between the number of beds and the price of the listing?
 
I created Density plot to  analyze it and find that there is a correlation between number of beds and price. Below are the p-value results which is less than 0.05 indicating we can reject null hypothesis that there is no relation between no of beds and price
P-value:	< 0.0001
Equation:	Price = 63.4681*Beds + 66.4977

Coefficients
Term	Value	StdErr	t-value	p-value
Beds	63.4681	1.10333	57.5241	< 0.0001
intercept	66.4977	1.9934	33.3589	< 0.0001

7.	What is the distribution of review scores ratings for Airbnb listings?
By using histogram we find the distribution is left skewed for ratings
8.	What is the distribution of Price for Airbnb listings?
By using histogram we find the distribution is right skewed for Price
11. Is there a relationship between the review scores rating and the price of the listing?
I created Density plot to analyze it and find that there is a correlation between ratings and price. There are some listings having very high values that is the skewing the data so if we use price excluding outliers we can see there is weak correlation between ratings and price.
Below are the p-value results which is less than 0.05 indicating we can reject null hypothesis i.e there is no relation between ratings and price
P-value:	< 0.0001
Equation:	Price = 1.00864*Review Scores Rating + 58.7801

Coefficients
Term	Value	StdErr	t-value	p-value
Review Scores Rating	1.00864	0.0782007	12.8981	< 0.0001
intercept	58.7801	7.22674	8.13369	< 0.0001


## Challenges 
•	Differentiating between Review Scores Rating (bin) and Review Scores Rating fields
•	Creating calculated fields took some time to understand in case there are complex calculations involved.

## Future Goals
This Airbnb dataset does not have the guests check in / check out data, occupancy data, facilities data for each location. We can proceed on further analysis by obtaining such dataset. Additionally, we can do comparison of different cities to check what are the different behavior in property type and prices.
