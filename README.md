# MomGulfing

MomGulfing is a simple momentum and candlestick pattern based trading strategy. Developed on [TradingView](https://www.tradingview.com/) with [PineScript](https://www.tradingview.com/pine-script-docs/en/v5/Introduction.html)

## Trading Decisions
### Opens a Long Position When;
- RED -> GREEN,
- Green close > previous red high,
- Green candle volume > previous red candle volume

#### or

- RED -> GREEN -> GREEN
- First green close < previous red high,
- Second green close > previous red high,
- Second green candle volume > previous red candle volume

#### or

- RED -> GREEN -> GREEN -> GREEN
- First green close < previous red high,
- Second green close < previous red high,
- Third green close > previous red high,
- Third green candle volume > previous red candle volume

### Opens a Short Position When;
- GREEN -> RED,
- Red close < previous green low,
- Red candle volume > previous green candle volume

#### or

- GREEN -> RED -> RED
- First red close > previous green low,
- Second red close > previous green low,
- Second red candle volume > previous green candle volume

#### or

- GREEN -> RED -> RED -> RED
- First red close > previous green low,
- Second red close > previous green low,
- Third red close < previous green low,
- Third red candle volume > previous green candle volume

## Risk Management
- First candle's low (for long positions) or high (for short positions) is [stop level](https://www.investopedia.com/terms/s/stop-lossorder.asp)
- [Take profit level](https://www.investopedia.com/terms/p/profittaking.asp) based on [Risk-reward](https://www.investopedia.com/terms/r/riskrewardratio.asp): 2.5 (default setting)
- [Leverage](https://www.investopedia.com/terms/l/leverage.asp) is 80/stop_loss_percent. Strategy uses all risk amount for the position. (If risking 1% of portfolio, enter position with that amount)
- Default [pyramiding](https://www.investopedia.com/terms/p/pyramiding.asp) is 3
- Update take profit/stop loss levels at each signal.

*For more details check [momgulfing.pine]() file*

## Backtests
*Default parameters are used in all backtests, on daily charts. Backtest period: 2021-01-01 -> 2022-12-31*

### BTC-USDT
![BTC-USDT](https://github.com/rasimandiran/momgulfing/blob/main/BTC-USDT.png?raw=true)
### ETH-USDT
![ETH-USDT](https://github.com/rasimandiran/momgulfing/blob/main/ETH-USDT.png?raw=true)
### BNB-USDT
![BNB-USDT](https://github.com/rasimandiran/momgulfing/blob/main/BNB-USDT.png?raw=true)
### XRP-USDT
![XRP-USDT](https://github.com/rasimandiran/momgulfing/blob/main/XRP-USDT.png?raw=true)
### AVAX-USDT
![AVAX-USDT](https://github.com/rasimandiran/momgulfing/blob/main/AVAX-USDT.png?raw=true)
### DOT-USDT
![DOT-USDT](https://github.com/rasimandiran/momgulfing/blob/main/DOT-USDT.png?raw=true)

## Usage (on [TradingView](https://www.tradingview.com/))

[MomGulfing Strategy](https://www.tradingview.com/script/T2bzelGR-MomGulfing/)

## References
- [Momentum Trading](https://www.investopedia.com/trading/introduction-to-momentum-trading/)
- [Candlestick Patterns](https://www.investopedia.com/trading/candlestick-charting-what-is-it/)

## License
[MIT](https://choosealicense.com/licenses/mit/)
