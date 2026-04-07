These two lines import essential tools for Time Series Analysis from the statsmodels library. They help you determine if your stock data is "predictable" or if it needs more cleaning.
## 1. from statsmodels.graphics.tsaplots import plot_acf

* What it is: A plotting tool for the Autocorrelation Function (ACF).
* The Logic: It creates a bar chart showing how a stock price today relates to its price yesterday, the day before, and so on (these are called "lags").
* Why you use it: It helps you see patterns. If the bars are high, the data has "memory." If they are within the shaded blue region, the relationship is just random noise.

## 2. from statsmodels.tsa.stattools import adfuller

* What it is: The Augmented Dickey-Fuller (ADF) statistical test.
* The Logic: It checks if your data is Stationary (meaning its mean and variance don't change over time).
* Why you use it: Most time-series models (like ARIMA) fail if the data isn't stationary.
* If the "p-value" from this test is < 0.05, your data is stationary (ready to model).
   * If it's > 0.05, your data has a "trend" (like a stock price generally going up), and you need to transform it first.

------------------------------
## 📝 Summary for your README:

| Tool | Function | Purpose |
|---|---|---|
| plot_acf | Visual Chart | Finds patterns/cycles in past data. |
| adfuller | Statistical Test | Checks if data is stable (stationary) enough to predict. |


