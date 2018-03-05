# Tutorial on Bitcoin and Ethereum price prediction

This tutorial is in 3 parts: 

   - The first model only includes financial-based features (extracted from coinmarketcap)
   - The second model includes Technical based features (block size ...)
   - The last one with complete our model by adding sentiment features in order to more accurately predict crash. 
   
### Model 1

### Data 

The training/test data is extracted from coinmarketcap. The feature of bitcoin can be used to predict the price of ethereum. This is due to the fact that currently the cryptomarket tends to rely on the bitcoin (the first cryptocurrency). For example, when the value of bitcoin goes down, other crytocurrencies often go down.
In addition, the pair system that exist in the cryptomarket (btc/xmr, btc/eth ...) link bitcoin currency to other altcoins. This model takes into account:

* btc_Close: the price of BTC
* bt_Volume: the volume of BTC
* bt_close_off_high: the gap between the closing price of BTC and price high for that day, where values of -1 and 1 mean the closing price was equal to the daily low or daily high, respectively.
* bt_volatility: the difference between high and low price of BTC divided by the opening price.
* eth_Close: the price of ETH
* eth_Volume: the volume of ETH 
* eth_close_off_high: the gap between the closing price of ETH and price high for that day, where values of -1 and 1 mean the closing price was equal to the daily low or daily high, respectively. 
* eth_volatility: the difference between high and low price of ETH divided by the opening price.

### Model 

We implemented a RNN with one LSTM cell.

## Dependency

We provide a dependancy file which can be used to run our model on floydhub

## Result 

Our LSTM model seems to have performed reasonably on the unseen test set. However the features of this training set are overly simple for a cryptocurrency price prediction price. We need to add technical based features (block size ...) in order to improve our model accuracy. 

## Model 2

Coming soon. 
