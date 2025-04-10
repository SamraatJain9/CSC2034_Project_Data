# CSC2034_Project_Data

## Task
Overview
You have been hired to consult for a winery in Portugal. They produce varieties of their traditional "Vinho Verde" and would like to understand what really determines their quality, so they can optimise their production.

The two datasets include 4899 and 1600 data points, respectively. Each data point is a set of 12 variables; 11 of these are physicochemical measures, and the last is the perceived quality (sensory output).

A fraction of each dataset is reserved for independent validation and will be used to make predictions on submissions, in addition to to checking that learning is done correctly (i.e., by separating training and test sets etc.). 

Your task is to create one or more models to predict quality given all other variables. To achieve this, you will:

1. Explore each of the two datasets: Do this by performing aggregations, computing summary statistics (using pandas), and plotting (with e.g. seaborn, matplotlib, or AltairLinks to an external site.) the data. Specifically, you should be able to:
 - Describe the distribution of wine quality across all samples, separately for red and white, and compare the quality distributions between reds and whites. Create suitable plots to illustrate.
 - Discretise the alcohol content variables (separately for whites and reds) into low, mid, high based on its distribution. Create a 3-valued "alcohol_cat" variable to represent this.
    - low < (average - stddev)
    - (average - stddev) < mid < (average + stddev)
    - high > (average + stddev)
 - Describe the distribution of wine quality as in (1.A), but separately for low-, mid-, and high-alcohol content. Create suitable plots to illustrate. Can you draw any conclusions on the relationship between alcohol content and quality?
 - Plot the residual sugar variable and identify a suitable threshold to separate "sweet" from "dry" wines*. Create a new "isSweet" binary variable to represent these two classes. The distributions of residual sugar are skewed for both reds and whites (in fact most wines in this dataset are dry according to the official definition, e.g., https://winefolly.com/deep-dive/sugar-in-wine-chart/)Links to an external site.. A practical approach in this case is to pick a threshold that splits the dataset (almost) evenly, as that will give you two balanced classes for your classifier. So your task is to find a threshold such that each class has approximately the same number of records.
 - Using the threshold from (1.D), repeat the distribution analysis of quality vs isSweet. Are sweet wines perceived as lower or higher quality than dry wines?