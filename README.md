# 📈 Yes Bank Stock Closing Price Prediction

## 📝 Project Overview
Yes Bank is a prominent private-sector bank in India. Since 2018, the bank has been in the news due to a major fraud case involving its founder, Rana Kapoor. This catastrophic event led to a massive crash in the bank's stock price, creating a "structural break" in its historical trend. 

This Machine Learning Capstone project aims to analyze the impact of this crisis and build a robust regression model to predict the stock's monthly closing price based on historical market data.

## 🎯 Business Objective
Stock price prediction is highly challenging due to market volatility. The goal of this project is to build a predictive model that can:
* Accurately forecast the monthly `Close` price.
* Handle the extreme multicollinearity present in stock features (`Open`, `High`, `Low`).
* Adapt to massive regime changes (like the 2018 market crash) to minimize financial risk.

## 📊 Dataset Description
The dataset consists of monthly stock prices of Yes Bank from its inception.
* **Date:** Month and Year of the record.
* **Open:** Opening price of the stock.
* **High:** Highest price during the month.
* **Low:** Lowest price during the month.
* **Close:** Closing price (Target Variable).

## 🛠️ Key Steps & Methodology
1. **Exploratory Data Analysis (EDA):** Visualized the 2018 structural break and proved the crash was statistically significant using Hypothesis Testing (T-Tests).
2. **Feature Engineering:** Created crucial time-series features like `Close_Lag1` (Previous Month's Price) and `Volatility` to give the model market "memory".
3. **Handling Multicollinearity:** Identified >0.98 correlation between independent variables using a Heatmap.
4. **Model Building:** Implemented Time-Based Splitting to train and evaluate:
   * Linear Regression
   * Ridge Regression (L2 Regularization)
   * Random Forest Regressor

## 🏆 Final Results & Conclusion
| Model | R2 Score | RMSE |
| :--- | :--- | :--- |
| Linear Regression | ~ 0.99 (Overfitted) | High |
| Ridge Regression | 0.57 | 82.12 |
| **Random Forest (Tuned)** | **0.97** | **21.68** |

* **Winner:** The **Random Forest Regressor** outperformed the linear models. 
* **Key Insight:** While the stock faced a massive crash, the Random Forest model successfully navigated it by heavily relying on the engineered `Close_Lag1` feature. This allowed the model to "learn" the price drop step-by-step rather than failing to extrapolate a linear trend.

## 💻 Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, SciPy
* **Techniques:** Regression Analysis, Time-Series Feature Engineering, GridSearchCV, Hypothesis Testing

## 👨‍💻 Author
**Sourabh Khamankar**
* [[LinkedIn Profile](https://www.linkedin.com/in/sourabh-khamankar)] *(Sourabh Khamankar)*
* [GitHub Profile](https://github.com/SourabhKhamankar22)
