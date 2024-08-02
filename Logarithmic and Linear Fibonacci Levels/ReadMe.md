# Introduction

Fibonacci levels are a technical analysis tool used by some traders to identify potential support and resistance levels. The principle for determining these levels is to take the distance between selected reference high and low points (swing high and swing low in general) as 1 unit and mark the ratios derived from the Fibonacci sequence, such as 0.236, 0.382, 0.618, etc., over this 1 unit.

In the conventional method of level determination, the 1 unit is divided into equal distances within itself, and Fibonacci levels are determined based on these equal distances. These types of levels are called **Linear Levels**. A relatively less common method involves dividing the 1 unit into progressively smaller, more accurately described as proportionally equal, distances and determining Fibonacci levels based on these distances. These types are called **Logarithmic Levels**. 

The purpose of this indicator is to provide ease of use in determining both Linear and Logarithmic levels.

# Where Can it be Used?

**Logarithmic Levels** can be used in any instrument where volatility is high for any reason. Specifically in crypto, Logarithmic Levels work very well for $BTC (to observe this, please study the wick from January 23, 2024). 

As another example, Logarithmic Levels can be used to identify potential accumulation and distribution schemes in altcoins with relatively high volume and market capitalization (refer to the chart $FETUSDT). Additionally, when analyzing traditional markets, Logarithmic Levels can be beneficial for stocks with highly inflated or deflated prices (e.g., $TSLA, $NVDA), in stock markets of countries battling high inflation (e.g., $XU100), or in currency pairs of countries experiencing a recession (e.g., $JPYUSD).

# How Can it be Used?

The indicator is designed similarly to the Fibonacci Tool provided by Trading View to ensure users feel familiar with it. When you start the indicator, select the reference levels (Level 1 and Level 0), then click on the indicator settings to choose specific levels and customize them according to your preferences.

# What Makes it Unique?

In the Fibonacci Tool provided by Trading View, both linear and logarithmic levels are visible. However, to view logarithmic levels, it is necessary to switch the relevant instrument's Super Chart to a logarithmic scale. This causes the levels we want to remain 'linear' to also be displayed in their logarithmic form, potentially leading to errors in other indicators we use, incorrect functioning of trend lines drawn in linear scaling, and so on. 

Additionally, when the Super Chart is scaled logarithmically, it prevents the ability to set alerts for prices and trend lines. This indicator was created to avoid these problems without needing to change the chart's scaling method and to allow the simultaneous viewing of both Linear and Logarithmic levels.


# Version Control

- The indicator is currently in the beta phase. Please report any bugs you encounter.

## Version 1.0.0

***Bugs***

- _(solved)_ The prices related to the Fibonacci levels calculated by the indicator may differ from the prices calculated by the Fibonacci tool provided by Trading View. However, this difference only occurs in the last decimal place. For example: 1.9764 -> 1.9765.
    - The Fibonacci tool provided by Trading View uses the `ceiling` function when calculating prices for the relevant levels. As a result, all prices are rounded up to the next significant decimal place. The indicator we created is more precise and performs more accurate rounding in this regard.
- _(unsolved)_ When the `endTime` parameter is manually increased from the indicator's settings to select a specific future date, the `Extend Left` option is automatically activated.
- _(unsolved)_ When the `endTime` parameter is manually increased from the indicator's settings to a future date beyond the current date, the horizontal level lines start from the `startTime` bar and extend infinitely to the left.
- _(unsolved)_ Optimization and cleaner script is needed to ensure that the indicator does not cause any run time errors, if new features is desired to be added. 


***Upcoming Features***

- _(not added)_ Add `noise` option. This option creates new levels by adding and subtracting a margin of error, determined by the user, to the prices corresponding to the Fibonacci levels. In cases where prices may not exactly touch the levels, this function provides traders with a more flexible and faster usage. However, we are first needed to optimize the script to ensure that the `noise` function does not cause any run time errors.
- _(not added)_ When `Labels Left` and `Extend Left` is enabled, show price labels at the left edge of the chart.
