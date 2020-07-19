Bot_trading_crypto


A simple strategy to make money by trading with cryptocurrency. This strategy includes:
1) buying ‘coins’ at a price x
2) selling them at the price of x * y % with y > 1.0

An assumption can be made that whatever price ‘coins’ are bought, if one waits long enough, whether that be one week, one month, or one year, one would have the opportunity to sell their ‘coins’ at a better price. This is obviously a questionable assumption as no one can predict the crypto currency market.

The graph below represents the evolution of the market capitalisation and the volume of trading. Note: market capitalisation = number of coins * price of the coins.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/market_capitalisation.png)

To prove my hypothesis, I created an algorithm to help me analyse how long it would take to gain a profit of y%. My goal was to find the optimal y. 

I simulated the following strategy between the first of January 2019 and the end of December 2019. With 10 000€ in a bank account I:
Bought ‘coins’ for 222 euros every sunday at 7AM (this date and time were chosen randomly)
Exchanged the ‘coins’ into euro as soon as the exchange rate increased by y%

Fees were included at 1% of the computation and the simulation was carried out with Bitcoins (BTC), Ethereum (ETH) and Litecoins (LTC). I aimed for the following target profit of: 5%, 10% and 15%.

In order to compare the results, I chose 29 March 2020 as the date in which to sell all the ‘coins’ at the market price. 

## Bitcoin

One can read on this graph: the balance of a bank account starting at 10 000€ which buys BTC for 1000€ per month, 222€ per week, from 1 January 2019 to 1 May 2020. The ‘coins’ were automatically sold as soon as a profit of 5, 10 or 15% was made. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/plot_strategies_btc.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 5%. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_btc_5.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 10%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_btc_10%.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 15%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_btc_15%.png)

## Ethereum

One can read on this graph: the balance of a bank account starting at 10 000€ which buys BTC for 1000€ per month, 222€ per week, from 1 January 2019 to 1 May 2020. The ‘coins’ were automatically sold as soon as a profit of 5, 10 or 15% was made. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/plot_strategies_eth.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 5%. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_eth_5%.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 10%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_eth_10%.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 15%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_eth_15%.png)

## Litecoin

One can read on this graph: the balance of a bank account starting at 10 000€ which buys BTC for 1000€ per month, 222€ per week, from 1 January 2019 to 1 May 2020. The ‘coins’ were automatically sold as soon as a profit of 5, 10 or 15% was made. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/plot_strategies_ltc.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 5%. 

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_ltc_5%.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 10%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshot/hist_days_ltc_10%.png)

The histogram below represents how long it takes to sell ‘coins’ by targeting a profit of 15%.

![alt text](https://github.com/henri45/crypto_bot/blob/master/screenshotshot/hist_days_ltc_15%.png)

The result are close in proximity to each other whatever cryptocurrency was used. This is due to the price of BTC, ETH and LTC being highly correlated. This simple strategy should be profitable in the long run, assuming that the price of the cryptocurrency will always hit a threshold which has been hit in the past. Although as depicted in the histogram, this might take a far amount of time.

One of the reasons this strategy doesn’t offer better results is the ‘coins’ are bought blindly every Sunday at 7AM. This variable has room for improvement. One could research which would be the best day to purchase ‘coins’. Even better, a bot could buy coins automatically if the market decreases for 3 days for instance. 

The fluctuation of the cryptocurrency offers other opportunities. Cryptocoins can be used as an intermediary for exchanging currencies. If someone would want to exchange South African Rands into Euros for instance, it will cost up to 5% with the a classic intermediary (SWIFT transfer, Paypal, etc.). Using a cryptocoin as an intermediary can be much cheaper.

## Using cryptocurrency as an intermediary for currency exchange

For example, if one want to exchange R3 000 each week into Euros, one could then buy cryptocurrency with the South African Rand and sale it against the Euro. The transaction fee could even be gained back by waiting for the crypto price to increase before selling them in Euros.

Here is the modelisation of this strategy, to make it simple the ‘coins’ are bought and sold in Euros. The logic would remain the same if the ‘coins’ were bought in another currency. The idea is to check how long it would take to make a 1% profit by selling the ‘coins’. This would permit one to do a currency exchange for free.

The histogram below represents how long it would take to hit a 1% profit. 

## Going further

This algorithm is a good base to test trading strategies. One could work on finding the best moment to buy ‘coins’ but also the best moment to sell them. Here is a list of a simple strategy that could be implemented:
Buy ‘coins’ when the exchange rate goes down by more than x % in y days.
Buy ‘coins’ if the exchange rate goes below a certain threshold 
To not buy ‘coins’ if the exchange rate goes above a certain threshold
Automatically sell ‘coins’ if the exchange rate increases by 3%, sell ‘coins’ if the exchange rate decrease by 2%

To conclude, it is a good idea to keep the cryptocurrency market in mind, as what was true in the past doesn’t necessarily mean it will be true in the future. This type of market still has many opportunities and is still taking off. It would be impossible for someone to predict it’s evolution. Therefore no one should invest money they cannot afford to lose. 
