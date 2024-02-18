# Gold Master EA

This is the code for the Gold Master EA developed by the Forex Robot Easy Team. This expert advisor is designed for trading gold (XAUUSD) on the H1 timeframe. It uses moving averages and trend lines to generate entry and exit signals.

## Libraries Used
The following libraries are included in this code:
- Trade: Provides functions for trading operations.
- MovingAverages: Calculates moving averages.
- TrendLine: Calculates trend lines.
- Notifications: Sends push notifications and emails.
- Backtesting: Allows for backtesting of the EA.

## Constants
The following constants are defined in this code:
- SYMBOL: The trading symbol, set to XAUUSD (gold).
- TIMEFRAME: The timeframe for trading, set to PERIOD_H1 (1 hour).
- LOT_SIZE: The lot size for trades, set to 0.01.
- RISK_PERCENTAGE: The percentage of account balance to risk per trade, set to 1%.
- STOP_LOSS: The stop loss distance in pips, set to 100 pips.
- TAKE_PROFIT: The take profit distance in pips, set to 200 pips.

## Object Initialization
The following objects are initialized in this code:
- trade: An instance of the CTrade class for executing trades.
- movingAverages: An instance of the CMovingAverages class for calculating moving averages.
- trendLine: An instance of the CTrendLine class for calculating trend lines.
- notifications: An instance of the CNotifications class for sending notifications.
- backtesting: An instance of the CBacktesting class for backtesting the EA.

## Entry and Exit Signals
The IsEntrySignal function calculates the moving average and trend line values and returns true if the moving average is above the trend line, indicating a bullish signal.

The IsExitSignal function calculates the moving average and trend line values and returns true if the moving average is below the trend line, indicating a bearish signal.

## Trade Execution
The ExecuteTrade function sets the entry price, stop loss price, and take profit price based on the current ask price and the defined stop loss and take profit distances. It then executes a buy stop order with the specified lot size, entry price, stop loss price, and take profit price.

## Trade Adjustment
The AdjustTradeParameters function calculates the risk amount based on the account balance and the defined risk percentage. It then sets the lot size based on the risk amount and the stop loss distance.

## Trade Monitoring
The MonitorTradePerformance function retrieves the current profit and account balance from the trade object and prints them to the console. It also sends a push notification and an email with the current profit.

## Main Function
The OnTick function is the main function that is called on each tick. It checks for an entry signal, and if one is found, it executes a trade and adjusts the trade parameters. It then checks for an exit signal, and if one is found, it closes all open trades. Finally, it monitors the trade performance.

## Backtesting Function
The OnTester function is the function that is called during backtesting. It sets the symbol, timeframe, initial deposit, and spread for the backtesting. It then starts the backtesting loop, calling the OnTick function on each iteration. Once the backtesting is finished, it prints a report with the results.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/gold-master-ea-review-effective-gold-trading-without-risks/). Note that ForexRobotEasy is not the official developer of this product. They only provide a review and sample code that can work as described in the product. To find the official developer of this product, please use MQL5.
