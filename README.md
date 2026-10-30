# TTC Strategy & TTC Optimiser

## 1. What is TTC Strategy?
<img width="1153" height="412" alt="Screenshot 2026-10-30 232503" src="https://github.com/user-attachments/assets/b1a52918-69be-48bb-b1bd-3183eb4d65fe" />

TTC Strategy is a trading strategy that identifies potential buying and selling opportunities based on market trends and support and resistance levels.

It uses custom calculations that combine trend analysis with support and resistance to generate trading signals.

The strategy displays its signals through coloured columns:

- **Green Columns:** Indicate a bullish signal and trigger a long (buy) trade.
- **Red Columns:** Indicate a bearish signal and trigger a short (sell) trade.

In simple terms, the strategy takes a long position when its columns turn green and a short position when they turn red.

The strategy has two adjustable inputs (Input 1 and Input 2). These inputs control its calculations and influence how it responds to market movements.

However, finding the right input settings can be challenging because market conditions and behaviour change over time. Settings that perform well on one symbol or timeframe may not perform equally well on another.

This is where TTC Optimiser comes in.

## 2. What is TTC Optimiser?
<img width="1281" height="615" alt="NIFTY_2026-10-30_23-38-36" src="https://github.com/user-attachments/assets/feb12be9-aec8-491a-b546-6b547f4a88f1" />


TTC Optimiser is a tool designed to find the best-performing input settings for TTC Strategy.

Like other trading indicators and strategies, TTC Strategy's performance can vary depending on market conditions, the trading symbol, and the timeframe. As market behaviour changes, its effectiveness can also change.

This makes it difficult to determine whether the current input settings are still suitable for the market or whether they need adjustment.

**TTC Optimiser solves this problem by automatically testing different combinations of input settings and identifying the ones that have performed best on the selected chart.**

### How Does TTC Optimiser Work?

TTC Strategy has two adjustable inputs:

- Input 1
- Input 2

TTC Optimiser tests **800 different combinations** of these two inputs.

For every combination, it runs a backtest of TTC Strategy using the available chart data and analyses the resulting performance report.

After comparing all 800 combinations, it identifies and displays the **top 5 best-performing parameter combinations** based on your selected performance criteria.

This allows you to quickly identify which settings have historically performed best for a particular symbol and timeframe without manually testing hundreds of combinations.

## How to Use the TTC Optimiser

### Steps

1. Add the **TTC Optimiser** to your chart.
2. Configure the optimisation settings according to your requirements.
3. Run the optimiser and note the best-performing parameters.
4. Enter the selected parameters into the **TTC Strategy**.
5. Review the strategy's backtest report to determine whether its performance meets your requirements.
6. If the results are satisfactory, consider using the strategy for further analysis or as part of your trading strategy.



**In simple terms:** TTC Strategy generates trading signals, while TTC Optimiser helps you find suitable input settings for that strategy by systematically testing and comparing different parameter combinations.

## 3. Optimiser Features

TTC Optimiser offers several features that allow you to configure how the best-performing parameters are identified and selected. Using these features, you can customise the optimisation process according to your trading preferences and requirements.

### A. Optimisation Criteria
<img width="318" height="173" alt="Screenshot 2026-10-26 113329" src="https://github.com/user-attachments/assets/0be29f69-b91a-468a-b301-a9b6b1137765" />


Different traders have different priorities. Some prefer strategies that generate higher profits, while others prioritise trading accuracy.

TTC Optimiser provides two main criteria for ranking parameter combinations:

**1. Highest Profitability**

Finds the parameter combinations that generated the highest profit during the backtest.

**2. Highest Accuracy**

Finds the parameter combinations that achieved the highest trading accuracy (win rate).

Based on your selection, the optimiser ranks the tested combinations and displays the top 5 results.

This gives you the flexibility to choose settings according to your trading preferences and objectives.

### B. Parameter Configuration
<img width="509" height="168" alt="Screenshot 2026-10-30 231050" src="https://github.com/user-attachments/assets/843b710e-1eca-4f82-991b-f0fa58aca691" />


TTC Optimiser provides a dedicated group of settings that allows you to configure which parameter combinations should be tested for TTC Strategy.

Using these settings, you can define the range of values and the steps between values for both Input 1 and Input 2.

This gives you control over the optimisation process and allows you to focus on the parameter ranges you want to explore.

### C. Filtering Optimisation Results
<img width="292" height="302" alt="Screenshot 2026-10-26 113120" src="https://github.com/user-attachments/assets/2f0016f5-ea68-4a6d-ac8a-162f9623b1a8" />


TTC Optimiser also provides several filters to help you narrow down the results and find parameter combinations that meet your requirements.

You can apply the following filters:

- **Minimum Trades:** Excludes parameter combinations that generated fewer trades than the specified minimum.
- **Maximum Trades:** Excludes parameter combinations that generated more trades than the specified maximum.
- **Minimum PnL:** Excludes parameter combinations whose profit and loss (PnL) is below the specified value.
- **Minimum Accuracy:** Excludes parameter combinations whose trading accuracy (win rate) is below the specified percentage.

When these filters are applied, the optimiser displays the top-performing parameter combinations that satisfy all the specified conditions.

**Example:** If you want to find profitable settings that generate at least 50 trades with an accuracy of 60% or higher, you can configure the filters accordingly.

### D. Backtesting Commission Settings
<img width="289" height="50" alt="Screenshot 2026-10-26 113438" src="https://github.com/user-attachments/assets/1d2b1c66-4cdc-4286-ae6b-1eb083911032" />


TTC Optimiser includes an input to configure the commission charged on each trade during backtesting.

This allows you to account for trading costs when evaluating the performance of different parameter combinations.

Commission is specified as a percentage and applied to both entry and exit transaction values.

**Formula:**

```text
Commission = (Commission Rate / 100)
             × (Entry Price + Exit Price)
```

For example, with a commission rate of 0.1%, an entry price of 100, and an exit price of 110:

```text
Commission = (0.1 / 100) × (100 + 110)
           = 0.21
```
### E. Long and Short Trade Settings
<img width="157" height="123" alt="Screenshot 2026-10-30 231433" src="https://github.com/user-attachments/assets/5c0140d6-10ed-4f8d-b24c-d176dd054a15" />


TTC Optimiser provides separate options to enable or disable long and short trades during optimisation.

This allows you to optimise TTC Strategy according to your preferred trading direction.

- **Both Long and Short Enabled:** Tests the strategy using both buying and selling trades.
- **Long Only:** Tests the strategy using only long (buy) trades.
- **Short Only:** Tests the strategy using only short (sell) trades.


## Important Note

**The optimiser identifies parameters based on historical backtesting results. Past performance does not guarantee future results.**

**Market conditions can change, and parameters that performed well historically may not continue to perform equally well in the future.**

**We recommend independently validating the selected parameters before using them in live trading.**
