---
description: Things i've learned about trading
---

# Trading
* Shares - buy part of a compnay, value dictates by supply/demand and future company success.
* Indecies - A group of shares
* Commodities - Gold/ Silver/ Sugar/  Oil/ Copper etc
* Forex - Buying USD with GBP. very volatile. Trillions traded a day, everyone needs other currencies. 

## IG
[IG Dashboard](https://www.ig.com/uk/myig/dashboard)
[IG Academy](https://www.ig.com//uk/learn-to-trade/ig-academy)
[IG API](https://labs.ig.com/)
[IG API companion][https://labs.ig.com/sample-apps/api-companion/index.html] (GUI for the API)
### Chart Types
* Line chart
Most basic, gives the closing price of an asset on that day
* HLOC (Bar Chart)
High, Low, Open, Close as the acronym suggests.
* Candle Stick Chart
Same as the HLOC but displayed in a different way
A green (or white) body shows the price has increased while a red (or black) body shows it has dropped
Long candle bodies and short wicks signify there's been strong buying or selling pressure in one direction
Short bodies and long wicks indicate there was significant buying or selling pressure in one direction, but that pressure then reversed
### Orders
An order is simply an instruction to buy or sell an asset. Once the order has been filled, it is called a 'filled order'.
### Limit orders
A limit order is an instruction to trade if a market's price reaches a particular level that's more favourable than the current price.
It is a may of getting out when you've made the profit you want
### Stop Order
It helps to 'stop losses'
Stop order is an instruction to trade when the market hits a level less favourable than the current price.
It is a way of getting out if it goes down too much. It allows you to know your maximum potentiall loss before you bet. 

* Good till cancelled (GTC)
Order remains valid until you cancel it yourself or the order is filled. On some exchanges, the order may only be valid for a specified period, so it may be worth checking with your broker.

* Good for the day (GFD)
Order remains active until the end of the trading day on which you place it. Check with your broker to see when your chosen market closes.

* Good till date/time
You must select a date and time when you want your order to be cancelled if it hasn't been filled.

* Fill or kill (FOK)
If the order can't be filled in full immediately, it will be cancelled.

* Execute and eliminate
As much of the order as possible will be filled at the price you specify. Any remaining part of the order will be cancelled.

### Leverage
Just as a mechanical lever helps you move a heavy load with only a small amount of force, leverage enables you to gain a large exposure to a financial asset using only a small amount of your trading capital.

## Spread betting and CFDs
### Financial Spread Betting
Financial spread betting is simply betting on how the value of a financial asset will change in the future. In most cases, you're betting on whether it will rise or fall. If you think the price of the asset will go up, you 'buy' (also known as going long). If you think it will fall, you 'sell' (go short).

You can buy as the 'Buy' Price and sell at the 'Sell' price. The gap between the two prices is called the *spread*.

Neither the buy price nor the sell price represents the exact value of the financial asset you're betting on (also known as the underlying asset). Instead, the buy price is slightly higher than this value, and the sell price is slightly lower.

The spread is essentially a fee that your spread betting provider charges to place your bet, and the narrower the spread, the better it is for you. Let's look at why.

## IG Interface

### EPIC
This is an instrument identifier.
"Our instruments are identified by proprietary EPICs, such as IX.D.FTSE.CFD.IP - this CFD contract shows that it is the FTSE100 cash price market."


## Automated Trading

* [Fully Automated IG](https://www.reddit.com/r/UKInvesting/comments/7q67cw/faig_fully_automated_ig_trading_a_python_script/) - see the github repo too

* [R cyrpto bot](https://towardsdatascience.com/build-a-cryptocurrency-trading-bot-with-r-1445c429e1b1)