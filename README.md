# Bike-Sharing Demand Analysis

## Project Overview

BoomBikes, a US bike-sharing provider, has experienced significant revenue dips due to the Corona pandemic. With the economy expected to recover post-lockdown, BoomBikes aims to strategically position itself to accelerate revenue by understanding and meeting the anticipated demand for bike-sharing.

The objective of this project is to model the demand for shared bikes with available independent variables, helping BoomBikes' management to strategize and align business operations to the market demand.

## Business Problem

The ongoing pandemic has drastically affected mobility and transportation industries, leading to a decreased demand for bike-sharing services. As the situation improves, understanding the factors influencing the demand will enable BoomBikes to efficiently cater to the market, optimizing their service and potentially increasing market share.

## Goals

1. Identify significant variables that predict the demand for shared bikes.
2. Quantify how well these variables describe the bike demands.

## Data Preparation

The dataset contains various features like weather conditions, user types, and temporal markers:

- **Categorical Variables:** Features like 'weathersit' and 'season' are encoded numerically but represent categories without inherent order and thus will be converted to categorical strings for analysis.
- **Year Variable ('yr')**: Indicates years 2018 (0) and 2019 (1). Despite its binary nature, it is crucial due to the increasing popularity of bike-sharing systems year over year.

## Columns of Interest

- `casual`: Number of casual users.
- `registered`: Number of registered users.
- `cnt`: Total number of bike rentals (target variable).

## Model Building

The model will predict the total daily bike rentals ('cnt') using the features provided in the dataset. Both linear and potentially more complex regression models will be considered to best fit the data.

## Model Evaluation

Model performance will be evaluated using the R-squared score to quantify how well the independent variables explain the variability of the target variable ('cnt').

```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)  # Replace y_test, y_pred with actual variable names used
