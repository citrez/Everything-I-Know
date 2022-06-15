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

## Notes of algo trading talk
### Links
[gist of the whole session](https://gist.github.com/yhilpisch/fcc2f4665cbae77904c03f66a10ba8a7)
[The talk slides](https://certificate.tpq.io/odsc_ldn_2022.pdf)
[Dr yves website](https://home.tpq.io/certificate-programs/pyalgo/)
[Algo trading in less than 100 lines of code](https://www.oreilly.com/content/algorithmic-trading-in-less-than-100-lines-of-python-code/) - this is an oriely article.
[oanda web-based trading](https://trade.oanda.com/)
[gist with the code](https://gist.github.com/yhilpisch/fcc2f4665cbae77904c03f66a10ba8a7) - this is also linked in the slides.
[The monitoring platform](https://home.tpq.io/aimachine/)
[Article about efficient market hypothosis](https://www.sciencedirect.com/science/article/abs/pii/S0169207003000128) - 




### Questions
- How is the upper bound of returns you've seen made using recreational algo trading. 
deployment. 
- What is the best pipeline for using a piece of logic, a piece of code for actually buying securities, derivatives etc in real time. 
- continuous monitoring. Is it possible to get that offline visualitation refreshed for online data. 
- What is the name of the job that does this type of thing


The talk is focusing on the deployment. 

you only need wifi and a couple of open source packages. 


Book recomendation - The man who solved the markets. Listen to this. 

Look at oanda trading account. The best API. The paper trading account is the same as the real one. 



We want to get the tails of the returns distribution correct. If we could just avoid the worst days, we would be doing extremely well. 
Use r as the baseline stategy

We may need to change our code going from ofline models (on hisotrical data), to online models (when we are actually trying to predict on live data).

We could thoeretically incrementally update our model when new data comes in, this is not what is done ehere. We train our model once using historical data, and then predict it on live data. 

Its all to do with the implementation. The strategy if super super complex. Annecdote of refinitiv when the strategy was implemented in 150 lines and the production code was 15,000 lines. 
Crypto has nice charachteristics. 24hr trading, great APIs.

Ideas are cheap, its having the robust infrastructure in place to deploy the strategy. 

