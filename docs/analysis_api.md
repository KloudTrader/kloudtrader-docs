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
| Analysis Functions (A-Z)|Status 
| -------------     |:-------------:|
| Accumulation/Distribution Index| ✅ 
| Absolute Price Oscillator| ✅ 
| Advance Decline Line| 🔜
| Advance Decline Ratio| 🔜
| Alpha |✅ 
| Annual Return| ✅ 
| Annual Sharpe Ratio|✅ 
| Annual Volatility| ✅ 
| Arnaud Legoux Moving Average| 🔜
| Aroon|✅ 
| Aroon Oscillator |✅ 
| Average Directional Movement Index|✅ 
| Average Directional Movement Index Rating|✅ 
| Average Price | ✅ 
| Average True Range| ✅ 
| Awesome Oscillator| ✅ 
| Balance of Power|✅ 
| Beta|✅ 
| Berke Ratio| 🔜
| Bollinger Bands|✅ 
| Calmar Ratio|✅ 
| CAGR (Compounded Annual Growth Rate)|✅ 
| Chaikin Money Flow|✅
| Chaikin Oscillator|✅
| Chande Kroll Stop| 🔜
| Chande Momentum Oscillator| ✅
| Choppiness Index| 🔜
| Commodity Channel Index| ✅
| ConnorsRSI| 🔜
| Coppock Curve|✅ 
| Conditional Sharpe ratio| 🔜
| Correlation Cofficient|✅ 
| Cumulative Returns |✅ 
| Cumulative Volume Index| 🔜
| Daily Returns|✅ 
| Daily Log Returns|✅ 
| Daily volatility|✅ 
| Detrended Price Oscillator| ✅
| Directional Movement Index|✅
| Donchian Channels|✅
| Double EMA |✅
| Downside Risk|✅ 
| Ease of Movement| ✅
| EMA|✅
| Envelope Indicator| 🔜
| Excess return on VaR| 🔜
| Expected shortfall| 🔜
| Fisher Transform| 🔜 
| Force Index| ✅
| Hilbert Transform - Instantaneous Trendline|✅
| Hilbert Transform - Dominant Cycle Period|✅
| Hilbert Transform - Dominant Cycle Phase|✅
| Hilbert Transform - Phasor Components|✅
| Hilbert Transform - SineWave|✅
| Hilbert Transform - Trend vs Cycle Mode|✅
| Hull Moving Average |✅ 
| Ichimoku Cloud|✅
| Information Ratio|✅ 
| Jensen's Alpha| 🔜
| Kaufman Adaptive Moving Average|✅
| Keltner Channels |✅
| Klinger Oscillator | 🔜
| Know sure thing/KST|✅
| Kurtosis|✅ 
| Least Squares Moving Average| 🔜
| Linear Regression |✅
| Linear Regression Angle|✅
| Linear Regression Intercept|✅
| Linear Regression Slope|✅
| Lower partial moments| 🔜
| MACD (Moving Average Convergence Divergence)|✅
| Mass Index |✅
| Max Drawdown|✅ 
| McGinley Dynamic | 🔜
| MidPoint over period|✅
| MidPoint Price over period|✅
| Minus Directional Indicator|✅
| Minus Directional Movement|✅
| Median Price|✅
| Momentum |✅
| Money Flow | ✅
| Moon Phases| 🔜
| Modigliani Ratio| 🔜
| Moving Average |✅
| Moving Volatility|✅ 
| Negative Volume Index|✅
| Normalized Average True Range|✅
| On Balance Volume|✅
| Omega Ratio|✅ 
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
| Returns| ✅ 
| Sharpe Ratio|✅ 
| Simple Moving Average|✅ 
| Skewness|✅ 
| SMI Ergodic Indicator | 🔜
| SMI Ergodic Oscillator | 🔜
| Sortino Ratio|✅ 
| Standard Deviation|✅ 
| Sterling Ratio| 🔜
| Stochastic Oscillator|✅ 
| Stochastic RSI|✅ 
| Tail Ratio|✅ 
| Time Series Forecast|✅ 
| Treynor ratio| 🔜
| TRIX|✅ 
| Triangular Moving Average|✅ 
| Triple EMA|✅ 
| True Range | ✅ 
| True Strength Indicator |✅ 
| Typical Price|✅ 
| Ultimate Oscillator |✅ 
| Upside-potential Ratio| 🔜
| Value at Risk (Variance-Covariance method)|✅ 
| Variance|✅ 
| Vertical Horizontal Filter| 🔜
| Volatility|✅ 
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

aapl_data=pd.DataFrame(OHLCV('AAPL','2018-01-01','2019-01-31')['history']['day'])

accumulation_distribution_index(aapl_data['high'],aapl_data['low'],aapl_data['close'],aapl_data['volume'])
```
```python
return type : Pandas Dataframe

0               NaN
1      3.252030e+07
2      4.959698e+06
3      2.035432e+06
4      2.219792e+07
5      8.146040e+06
6      8.897564e+06
            ...
249    1.522707e+07
250   -2.311396e+07
251    3.982507e+06
252   -1.426856e+06
253    1.025702e+07
254    3.727678e+07
255    2.632004e+07
256    3.347596e+07
257    2.911781e+07
258    1.147651e+07
```
***
### Absolute Price Oscillator
Absolute Price Oscillator is a technical indicator calculating the percentage difference between two price moving averages. The Absolute Price Oscillator is the MACD indicator in absolute values.<br><br>
<a href="https://www.marketvolume.com/technicalanalysis/apo.asp" target="_blank">Learn More</a>

<code>absolute_price_oscillator(close,short_period,long_period)</code>

| Paramters       | Required/Optional | Description                             | Type |
|-----------------|-------------------|-----------------------------------------|------|
| close           | required         | Close prices data       | Pandas dataframe  |
| short_period    | reqired          | Short Period/Fast Period | int|
| long_period     | reqired          | Long period/Slow period | int |


```python
Example:

from kloudtarder.analysis import absolute_price_oscillator
from kloudtrader.equities.data import OHLCV
import pandas as pd

aapl_data=pd.DataFrame(OHLCV('AAPL','2018-01-01','2019-01-31')['history']['day'])

absolute_price_oscillator(aapl_data['close'],4,9)
```
```python
return type : Pandas Dataframe

0           NaN
1           NaN
2           NaN
3           NaN
4           NaN
5           NaN
6           NaN
7           NaN
8      0.334722
9     -1.698611
10    -3.473056
11    -4.962222
12    -3.864444
13    -1.796111
14     0.976944
15     2.807778
16     4.387500
17     4.363889
18     2.678056
19     1.762778
20     0.827500
        ...
254    2.469444
255    2.129722
256    4.135556
257    4.622500
258    4.882222
```
***
### Alpha
Alpha is a measure of the active return on an investment, the performance of that investment compared with a suitable market index. An alpha of 1% means the investment's return on investment over a selected period of time was 1% better than the market during that same period; a negative alpha means the investment underperformed the market.<br><br>
<a href="https://en.wikipedia.org/wiki/Alpha_(finance)" target="_blank">Learn More</a>

<code>alpha(close,benchmark_close)</code>

| Paramters       | Required/Optional | Description                             | Type |
|-----------------|-------------------|-----------------------------------------|------|
| close           | required         | Close prices data       | Pandas dataframe  |
| benchmark_close   | reqired          | Close prices data of market or benchmark like SPY, etc | Pandas dataframe |



```python
Example:

from kloudtarder.analysis import alpha
from kloudtrader.equities.data import OHLCV
import pandas as pd

aapl_data=pd.DataFrame(OHLCV('AAPL','2018-01-01','2019-01-31')['history']['day'])
spy_data=pd.DataFrame(OHLCV('SPY','2018-01-01','2019-01-31')['history']['day'])

alpha(aapl_data['close'],spy['close'])
```
```python
return type : Int

-17.984671751710962
```

***
### Annual Return
Annual return is the return an investment provides over a period of time, expressed as a time-weighted annual percentage.<br><br>
<a href="https://www.investopedia.com/terms/a/annual-return.asp" target="_blank">Learn More</a>

<code>alpha(close,benchmark_close)</code>

| Paramters       | Required/Optional | Description                             | Type |
|-----------------|-------------------|-----------------------------------------|------|
| close           | required         | Close prices data for a year i.e. trading days<257 and trading days>250      | Pandas dataframe  |
| benchmark_close   | reqired          | Close prices data of market or benchmark like SPY, etc | Pandas dataframe |



```python
Example:

from kloudtarder.analysis import alpha
from kloudtrader.equities.data import OHLCV
import pandas as pd

aapl_data=pd.DataFrame(OHLCV('AAPL','2018-01-01','2019-01-31')['history']['day'])
spy_data=pd.DataFrame(OHLCV('SPY','2018-01-01','2019-01-31')['history']['day'])

alpha(aapl_data['close'],spy['close'])
```
```python
return type : Int

-17.984671751710962
```