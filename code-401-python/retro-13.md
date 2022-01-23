# Retro 13: Linear Regression - 01/22/2022

Today, I was introduced `pylearn` library. It is a powerful python module for machine learning. It contains function for regression, classfication, clustering, model selection and dimensionality reduction. For lab 13, I analyzed historical apple stock price from 1980 to 2020 and tried to find out the trend. I used `Date` as x-axis and `Close price` as y-axis. One thing didn't go well was `lm.predict(x_test)` came back with error. It looks like `lm.predict` function cannot handle date type. I will do further investigation on this.
