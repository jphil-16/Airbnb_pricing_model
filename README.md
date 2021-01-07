# Airbnb Pricing Model

## Introduction
Is my Airbnb listing priced accurately??

This is a good question that a lot of people want to know. Airbnb has listings in over 100,000 cities worldwide and there are 660,000 listings in the United States alone. Most Airbnb hosts are normal people who might not know how to price their listing, and simply matching local hotel room prices usually won’t work...so what does?

This model uses Airbnb listing data from Inside Airbnb to predict the nightly booking rate for listings in the Seattle area. The following features are used in the model:
* Number of beds
* Number of bathrooms
* Total number of people that can stay
* Room type (entire home, private room, shared room, etc.)
* Host response time (within an hour, within a day, etc.)
* Neighborhood
* Whether the host is labeled a Superhost
* Whether the listing can be booked instantly
* Number of reviews
* Average number of reviews per month
* Review rating

If you plug in these values for your airbnb listing, this model will spit out a recommended nightly rate for your listing to make sure your property is competitve without leaving money on the table.

## The data
Inside Airbnb is an independent project that aggregates and analyzes publicly available Airbnb data. This model only used data from the Seattle area, and left out a few particular types of listings for simplification:
* Luxurylistings (anything over $400/night)
* Abandoned listings (no reviews from the past year)
* Hotel listings (some hotels list on Airbnb as well)

Removing these rows from the dataset still left the model with ~2500 rows of data utilize. There was still some data cleaning left to perform, including using one-hot encoding to transform the categoricial features, but then the models were ready for training.

## Which Model to Use?
Four different types of models were compared to make sure the best model type was selected: Linear Regression (OLS), K-Nearest Neighbors, Random Forest, and Gradient Boosting. After tuning each model, the Gradient Boosting model pereformed the best with an accuracy of 0.7. The most important features in the model were:
1. Number of people that can stay
2. Number of bathrooms
3. Average review rating

## Real World Application
In order to give the model a real-world test drive, I plugged in some standard information representing a 1 bed/1 bath apartment in the Queen Anne neighborhood. Assuming that the listing was relatively new to Airbnb (only a few reviews), the model's recommended price was $105 per night. This seems reasonable, but what happens if we take the same listing but assume that it is very established with a large number of positive reviews and a "Superhost" status? In that case, the recommended price jumped to $135 per night! This result is not only very useful as a business planning tool, it also passes the logic test and shows that our model is operating smoothly.

## Next Steps:
Here are a few possible improvements to make the model much more useful in the future:
* Add weights for bathroom types (private vs shared bathrooms, half-baths vs full-baths, etc.)
* Expand to cities other than Seattle
* Use text analysis to identify key phrases in the listing descriptions and reviews
* Adjust for missing data instead of eliminating it

