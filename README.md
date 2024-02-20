# Customer Lifetime Value
Forecasting Number of transactions a customer would make using Beta Geometric-Negative Binomial Distribution, a BTYD-Probabilistic Model.

## Overview
Trained a Beta Geometric-Negative Binomial Distribution (BG/NBD) model that explains how frequently customers make purchases while they are still "alive" and how likely a customer is to churn in any given time period, using customer transactions of E-Commerce store Olist [public dataset](https://www.kaggle.com/olistbr/brazilian-ecommerce).

**Model Outcome**
Trained Model Predicts Number of Purchases with an RMSE of 0.144 and is able to capture 99% of customer historical transactions with a frequency less than or equal to 4, and only less than 1% of customers have greater than 4 repeated purchases in the dataset.

## Model Architecture
The BG/NBD model is a probabilistic model that assumes customer purchase behavior follows a geometric distribution for the interval between purchases and a negative binomial distribution for the number of repeat transactions. The model parameters include:
- \( p \): Probability of making another purchase in the next time period.
- \( r \): Number of repeat transactions before churn.

## Assumptions
1. Customers make purchases independently of each other.
2. The probability of a customer making another purchase decreases over time.
3. The number of repeat transactions follows a negative binomial distribution.

## Limitations
1. Assumes constant purchase behavior over time, which may not hold in reality.
2. Does not account for external factors that could influence purchase behavior.
3. May not perform well with small datasets or highly skewed data distributions.

## Future Work
- Incorporate customer demographics and other features to improve model accuracy.
- Explore alternative models like Gamma-Gamma for estimating average transaction value.
- Conduct a sensitivity analysis to understand the impact of different parameter values on model predictions.

## About Olist Dataset

The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil, the orders are divided into 9 .csv files in a relational database schema.

For this study, I have aggregated data using the following 3 .csv files out of the 9 in the zip file.
* olist_customers_dataset.csv
* olist_orders_dataset.csv
* olist_payments_dataset.csv

**Source :** [Olist Dataset](https://www.kaggle.com/olistbr/brazilian-ecommerce)


## Setup Instructions

#### Creating Python Environment

This repository has been tested on Python 3.7.6.

1. Cloning the repository:

`git clone https://github.com/sjstheesar/customer_lifetime_value-bgnbd.git`

2. Navigate to the git clone repository.

`cd customer-lifetime-value-bgnbd`

3. Download raw data from the data source link and place in "datasets" directory

4. Install [virtualenv](https://pypi.org/project/virtualenv/)

`pip install virtualenv`

`virtualenv clv`

5. Activate it by running:

`clv/Scripts/activate`

6. Install project requirements by using:

`pip install -r requirements.txt`

**Note**
* For make_dataset(), please place the unzipped raw data (from data source) in the 'datasets' directory.

Updated on 2024-04-01T06:19:03+06:55
Updated on 2024-04-17T20:22:05+06:55
Updated on 2024-03-09T07:21:30+06:55
Updated on 2024-07-05T19:50:45+06:55
Updated on 2024-02-03T20:05:28+06:55
Updated on 2024-08-16T08:37:10+06:55
Updated on 2024-05-30T21:24:48+06:55
Updated on 2024-10-11T17:41:40+06:55
Updated on 2024-02-27T18:52:54+06:55
Updated on 2024-06-26T04:31:48+06:55
Updated on 2024-04-05T17:33:06+06:55
Updated on 2024-03-05T05:11:32+06:55
Updated on 2024-07-28T17:17:37+06:55
Updated on 2024-02-23T04:27:43+06:55
Updated on 2024-02-21T06:41:31+06:55