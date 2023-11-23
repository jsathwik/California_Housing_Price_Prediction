![plot](./results/California_Housing.jpg)

# California Housing Price Prediction 🏠🏠

Main theme of this project is to build linear regression model that predicts house prices in California based on housing features like median income, house age, rooms per household, Average Bedrooms, Latitude etc.

## Data 
The California housing dataset consists of `20640` data points, with each datapoint having `8 features`. This dataset was obtained from the StatLib repository -
[Dataset_Link](https://www.dcc.fc.up.pt/~ltorgo/Regression/cal_housing.html)  

This dataset was derived from the 1990 U.S. census, using one row per census
block group. A block group is the smallest geographical unit for which the U.S.
Census Bureau publishes sample data (a block group typically has a population
of 600 to 3,000 people).

A household is a group of people residing within a home. The average
number of rooms and bedrooms in this dataset are provided per household.


**Features Description**

1. `MedInc`     : median income in block group
2. `HouseAge`   : median house age in block group
3. `AveRooms`   : average number of rooms per household
4. `AveBedrms`  : average number of bedrooms per household
5. `Population` : block group population
6. `AveOccup`   : average number of household members
7. `Latitude`   : block group latitude
8. `Longitude`  : block group longitude

**Target** : `Median house value` - for California districts, expressed in hundreds of thousands of dollars ($100,000).

[California Housing Dataset in Sklearn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)

## Libraries Used 

**Language:** ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

**Packages:** ![sklearn](https://img.shields.io/badge/scikit-learn-orange)

## Implementation Details 📜

1. Housing data can be loaded into the code by first importing `sklearn.datasets.fetch_california_housing` module , using  `fetch_california_housing()` function.

2. Use `dataset.DESCR` to understand data or Use [California Housing Dataset Sklearn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html) for further details.

3. Segregate `Features` and `Target Variables` as `X`, `Y` respectively.

4. Using `sklearn.model_selection.train_test_split` split the X, Y into `train` and `test` data with defined `test_size` param as  `0.20`. Its is recommended to use `random_state` param to produce `same results` across all executions.

5. From the [California Housing Dataset Sklearn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html) it is evident that Feature values are `real` (but not within any limits). I have used `sklearn.preprocessing.StandardScaler` to bring them into limits.

6.  `sklearn.linear_model.LinearRegression` module is used for implementing `Regressor Model`. 

7.  Later `r2_score` and `mean_squared_error` (`Regressor Model Evaluation metrics`) are obtained.

## Evaluation and Results 🔍

| Metric        | Value         |
| ------------- | ------------- |
| R2 Score      | 0.57          |
| MSE           | 0.55          |

From the above `R2_score` it can be referred that `57%` of the changeability of the dependent output attribute can be explained by the model while the remaining 43 % of the variability is still unaccounted for.

## ⚡Key Takeaways⚡

Importance of the Dataset information in differentiating the Target and Features from the whole dataset, background of the data.

Good understanding of various packages of sckit-learn library required in implementing Regressor Model

Interpret the Evaulation metrics w.r.t Regressor model.

## ❓ FAQs ❔

#### How does the linear regression model work ?
Linear Regression relationship between the independent variable X and the dependent variable (response)  y is assumed to be linear. The linear relationship is represented by the equation: y=mx+b, where m is the slope (coefficient) and b is the intercept.

Linear relationship is extended to multiple Features (X1, X2, X3... Xn)
y = b0+ b1X1+b2X2+...+bnXn. where b0 is intercept , b1,b2,b3...bn are the coefficient of Features X1, X2, X3, X4 .. Xn

The objective is to find the values of b0,b1,b2,b3...bn, hat minimize the difference between the predicted y and the actual y for each data point.

#### What are R2_score and mean_squared_error metrics ?
`R2_score` quantifies the percentage of the dependent variable’s variation that the model’s independent variables contribute to. R2 is a useful statistic for evaluating the overall effectiveness and explanatory power of a regression model.

 `mean_squared_error` measures the square root of the average discrepancies between a dataset’s actual values and projected values.

When using these metrics, a `higher R2_score` and a `lower MSE` generally indicate better model performance, but it's essential to consider the context of your specific problem and the trade-offs between different evaluation metrics.

## Roadmap 🏁
1. Application of Feature Engineering techniques to increase the overall effectiveness of the model
2. Implementation of Decision tree model for the same problem statement

## Acknowledgements 🙌

- [Everything-you-need-to-know-about-Linear-Regression](https://www.analyticsvidhya.com/blog/2021/10/everything-you-need-to-know-about-linear-regression/)
- [regression-metrics](https://www.geeksforgeeks.org/regression-metrics/)
- [scikit-learn California Housing Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html#sklearn.datasets.fetch_california_housing)

## Contact

If you have any feedback/are interested in collaborating, please reach out to me via [📧](sathwik.office@gmail.com)


## License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)








