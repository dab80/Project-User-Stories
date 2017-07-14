# Project-User-Stories
```
Description:
Display time series charts of 3rd party historical stock prices along with several technical analysis indicators (TA).  TA indicators will be calculated from price data and stored for display when requested.

User Stories:
• UI - Provide lists of Index components, Index Sectors, Sector components
    ○ Determine NASDAQ, S&P 500, and DJIA components and store in MySQL 
• UI - Allow user to create and update lists of stocks, forex currency pairs, index futures (Name, symbol, date range)
    ○ Read/write/update via API to MySQL
• UI - Allow user to import lists of stocks, forex currency pairs, index futures (Name, symbol, date range)
    ○ Import into a new list or overwrite an existing list.
• Historical minute data - Using user lists, request and store (n) weeks of time series minute data (O, H, L, C, V) from 3rd party API.
    ○ Request Barchart, Google, or Yahoo 3rd party time/sales minute data (Open, High, Low, Close, Volume)
    ○ Consume retrieved 3rd party data and if needed, reformat UNIX time format into a usable format.
      - MySQL - Store original/raw data for future purposes such as handling stock splits.
    ○ Convert retrieved 3rd party data to percent change format
      - MySQL - Store percent change formatted data
    ○ Update nightly after close in market and/or possibly update intra-day in real-time.
• UI - Display stock/index time series charts allowing user to select 1, 5, and 15 minute charts
    ○ Use open source charting package just as highcharts or googlecharts
    ○ If time permits, allow for multiple times series on a single chart 
• UI - Calculate and display in separate panel(s) below the several indicators from user input values, as time allows:
    ○ SMA/EMA - Simple/Exponential moving average 
    ○ VWAP - Volume weighted average price
    ○ MACD - Moving average convergence/divergence
    ○ MFI - Money Flow Indicator
    ○ Aroon Indicator - 
    ○ Stochastic Oscillator
• Calculate profit/loss, return on investment, etc. for several canned long entry/exit & short entry/exit 
Stock profile data - Request and store profile data (shares outstanding, market capitalization) 
```
