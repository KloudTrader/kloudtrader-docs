---
id: analysis_api
title: Analysis
sidebar_label: Analysis
---

## Technical, portfolio, risk analysis APIs for your quantitative trading algorithms.
> #### Important
> 
> The algorithm you want to deploy should be in a file called **main.py**
> 
> Your algorithm must have these imports:
> 
> **from libkloudtrader.defaults import ACCESS_TOKEN, ACCOUNT_NUMBER**
> 
> This will help Narwhal to access your access token and account number from the Narwhal Environment so that you don't have to explicitly pass them with each API call. Narwhal would not be able to load your access token and account number from the Narwhal Environment if you don't link your tradier account. So the best practice is to link your tradier account before deploying your Trading Algorithm.

> Note: Your access token will expire after 24 hours. In order to allow your deployed algorithm to trade seemlessly, please manually link your tradier account after 24 hours. Don't worry this is just in Beta Version and will be automated soon!       
### Analysis API Index
#### libkloudtrader provides various analysis APIs. The list below consists of the APIs that are currently implemented and the ones that are coming soon!
| Analysis Functions|Status 
| -------------     |:-------------:|
| [Accumulation/Distribution Index](#accumulation-distribution-index)| ✅ 
| Absolute Price Oscillator| ✅ 
| Advance Decline Line| 🔜
| Advance Decline Ratio| 🔜
| Returns| ✅ 
| Annual Returns| ✅ 
| Volatility|✅ 
| Annual Volatility| ✅ 
| Daily volatility|✅ 
| Moving Volatility|✅ 
| Arnaud Legoux Moving Average| 🔜
| Aroon|✅ 
| Aroon Oscillator |✅ 
| Average Directional Movement Index|✅ 
| Average Directional Movement Index Rating|✅ 
| Average Price | ✅ 
| Average True Range| ✅ 
| Awesome Oscillator| ✅ 
| Balance of Power|✅ 
| Bollinger Bands|✅ 
| Chaikin Money Flow|✅
| Chaikin Oscillator|✅
| Chande Kroll Stop| 🔜
| Chande Momentum Oscillator| ✅
| Choppiness Index| 🔜
| Commodity Channel Index| ✅
| ConnorsRSI| 🔜
| Coppock Curve|✅ 
| Correlation Cofficient|✅ 
| Cumulative Return |✅ 
| Cumulative Volume Index| 🔜
| Daily Returns|✅ 
| Daily Log Returns|✅ 
| Detrended Price Oscillator| ✅
| Directional Movement Index|✅
| Donchian Channels|✅
| Double EMA |✅
| Ease of Movement| ✅
| EMA|✅
| Envelope Indicator| 🔜
| Fisher Transform| 🔜 
| Force Index| ✅
| Hull Moving Average |✅ 
| Ichimoku Cloud|✅
| Kaufman Adaptive Moving Average|✅
| Keltner Channels |✅
| Klinger Oscillator | 🔜
| Know sure thing/KST|✅
| Least Squares Moving Average| 🔜
| Linear Regression |✅
| Linear Regression Angle|✅
| Linear Regression Intercept|✅
| Linear Regression Slope|✅
| MACD (Moving Average Convergence Divergence)|✅
| Mass Index |✅
| McGinley Dynamic | 🔜
| MidPoint over period|✅
| MidPoint Price over period|✅
| Minus Directional Indicator|✅
| Minus Directional Movement|✅
| Median Price|✅
| Momentum |✅
| Money Flow | ✅
| Moon Phases| 🔜
| Moving Average |✅
| Negative Volume Index|✅
| Normalized Average True Range|✅
| Hilbert Transform - Instantaneous Trendline|✅
| Hilbert Transform - Dominant Cycle Period|✅
| Hilbert Transform - Dominant Cycle Phase|✅
| Hilbert Transform - Phasor Components|✅
| Hilbert Transform - SineWave|✅
| Hilbert Transform - Trend vs Cycle Mode|✅
| On Balance Volume|✅
| Parabolic SAR|✅
| Percentage Price Oscillator|✅
| Pivot Points HIgh Low| 🔜
| Plus Directional Indicator|✅
| Plus Directional Movement|✅
| Positive Volume Index| 🔜
| Rate of Change |✅ 
| Relative Strength index|✅ 
| Relative Givor Index| 🔜
| Relative Volatility Index| 🔜
| Simple Moving Average|✅ 
| SMI Ergodic Indicator | 🔜
| SMI Ergodic Oscillator | 🔜
| Standard Deviation|✅ 
| Stochastic Oscillator|✅ 
| Stochastic RSI|✅ 
| Time Series Forecast|✅ 
| TRIX|✅ 
| Triangular Moving Average|✅ 
| Triple EMA|✅ 
| True Range | ✅ 
| True Strength Indicator |✅ 
| Typical Price|✅ 
| Ultimate Oscillator |✅ 
| Variance|✅ 
| Vertical Horizontal Filter| 🔜
| Volatility Stop| 🔜
| Volume Osciallor | 🔜
| Volume Price Trend|✅ 
| Volume adjusted moving average|✅ 
| Volume weighted moving average| 🔜
| Vortex Indicator |✅ 
| VWAP|✅ 
| Weighted Close Price|✅ 
| Williams %R|✅ 
| Williams Aligator | 🔜
| Williams Fractal | 🔜
| WMA|✅ 
| Zig Zag | 🔜
| Cumulative Returns |✅ 
| Sharpe Ratio|✅ 
| Annual Sharpe Ratio|✅ 
| Calmar Ratio|✅ 
| Sortino Ratio|✅ 
| Skewness|✅ 
| Kurtosis|✅ 
| Omega Ratio|✅ 
| Tail Ratio|✅ 
| Value at Risk (Variance-Covariance method)|✅ 
| Alpha |✅ 
| Beta|✅ 
| Jensen's Alpha| 🔜
| Information Ratio|✅ 
| Modigliani Ratio| 🔜
| Expected shortfall| 🔜
| Lower partial moments| 🔜
| Treynor ratio| 🔜
| Excess return on VaR| 🔜
| Conditional Sharpe ratio| 🔜
| Upside-potential Ratio| 🔜
| Sterling Ratio| 🔜
| Berke Ratio| 🔜
| CAGR (Compounded Annual Growth Rate)|✅ 
| Max Drawdown|✅ 
| Downside Risk|✅ 

# Module
<code>libkloudtrader.analysis</code>

### Accumulation/Distribution Index
Developed by Marc Chaikin, the Accumulation Distribution Line is a volume-based indicator designed to measure the cumulative flow of money into and out of a security.<br><br>
<a href="https://stockcharts.com/school/doku.php?id=chart_school:technical_indicators:accumulation_distribution_line" target="_blank">Learn More</a>

<code>accumulation_distribution_index(high,low,close,volume)</code>

| Paramters       | Required/Optional | Description                             | Type |
|-----------------|-------------------|-----------------------------------------|------|
| high         | required          | High prices data       | Pandas dataframe  |
| low          | reqired          | Low prices data | Pandas dataframe|
| close          | reqired          | Close Prices data | Pandas dataframe  |
| volume          | reqired          | Volume data  | Pandas dataframe  |

```python
Example:

from kloudtarder.analysis import accumulation_distribution_index
from kloudtrader.equities.data import OHLCV
import pandas as pd

aapl_data=pd.DataFrame(OHLCV('FB','2018-01-01','2019-01-31')['history']['day'])

```
```python
return type : Pandas Dataframe


```