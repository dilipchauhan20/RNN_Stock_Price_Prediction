# RNN_Stock_Price_Prediction
> A case study to predict the stock prices using historical data from four companies (i.e. IBM, Google, Amazon, and Microsoft)

## Table of Contents
* [General Info](#general-information)
* [Data Description](#data-description)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
The objective of this assignment is to try and predict the stock prices using historical data from four companies IBM (IBM), Google (GOOGL), Amazon (AMZN), and Microsoft (MSFT).

We use four different companies because they belong to the same sector: Technology. Using data from all four companies may improve the performance of the model. This way, we can capture the broader market sentiment.

The problem statement for this assignment can be summarised as follows:

> Given the stock prices of Amazon, Google, IBM, and Microsoft for a set number of days, predict the stock price of these companies after that window.


### Data Description

We have been provided with four CSV files corresponding to four stocks: AMZN, GOOGL, IBM, and MSFT. The files contain historical data that were gathered from the websites of the stock markets where these companies are listed: NYSE and NASDAQ. The columns in all four files are identical. Let's take a look at them:

- `Date`: The values in this column specify the date on which the values were recorded. In all four files, the dates range from Jaunary 1, 2006 to January 1, 2018.

- `Open`: The values in this column specify the stock price on a given date when the stock market opens.

- `High`: The values in this column specify the highest stock price achieved by a stock on a given date.

- `Low`: The values in this column specify the lowest stock price achieved by a stock on a given date.

- `Close`: The values in this column specify the stock price on a given date when the stock market closes.

- `Volume`: The values in this column specify the total number of shares traded on a given date.

- `Name`: This column gives the official name of the stock as used in the stock market.

There are 3019 records in each data set. The file names are of the format `\<company_name>_stock_data.csv`.


## Technologies Used
- Python
- Numpy
- Panda
- Matplotlib
- Seaborn
- Sklearn
- Tensorflow
- Keras
- glob
- Jupyter Notebook


## Conclusions
After evaluating and comparing simpleRNN and LSTM models for predicting Amazon (AMZN) stock closing prices, the following insights and conclusions were drawn:

**Model Comparison Summary**

- Model Best Configuration Test MAE Test RMSE Test R² Score
- Simple RNN (units=50, dropout=0.2) 87.86 113.77 0.5976
- LSTM (units=32, dropout=0.2, lr=0.001) 45.04 56.97 0.8991

**Key Observations**

The LSTM model significantly outperformed the Simple RNN in terms of:

- Accuracy (lower MAE & RMSE)
- Model fit (R² score of ~0.90)
- Capturing long-term dependencies, which is essential in financial time series.

Simple RNN, while showing reasonable short-term trend tracking, suffered from:

- Higher error
- Underestimation of price spikes
- Lag in response to strong upward trends

**Visual Insights**

- From the actual vs predicted stock price plots:
- LSTM predictions closely follow the actual trend with less deviation.
- Simple RNN predictions consistently lag behind, especially during rapid trend shifts.

**Final Conclusion**

- The LSTM model is the preferred architecture for stock price prediction in this task due to its ability to:
- Model sequential dependencies effectively
- Provide lower error on unseen test data
- Generalize better to real-world price patterns



## Acknowledgements

- https://pandas.pydata.org/docs/user_guide/basics.html
- https://matplotlib.org/stable/tutorials/pyplot.html#sphx-glr-tutorials-pyplot-py
- https://seaborn.pydata.org/tutorial/introduction.html



## Contact
Created by [Dilip Chauhan](#dilipchauhan20ymail.com) - feel free to contact me!

