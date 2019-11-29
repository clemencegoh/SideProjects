# Algo Trading

## Evolution of trading
* Human
    * Broker (old fashioned)
* Model
    * Trade Indicators
* Computer
    * Trade execution

## Algo trading
* Integration of model and computer

## 2 different kinds
* Human-driven
    * Optimized execution
    * Risk management
* Fully automatic
    * By frequencies

## Why do we need algo services?
* Pressence of predatory algos


## Market making
* Highly affected by demand-supply
    * Market makers help to fill this gap by buying first from sellers and selling to buyers later
        * Makes money from "Profit from spreads"
        * Also takes risks: "Adverse selection risk"
            * Due to this, try not to carry overnight risks
            * **To ease their burden**: Designated market makers have obligations but receive rebates or compensation from exchanges
            * Top 10 come from private companies (Grasshopper from Singapore)

## Alpha seeking
* Earning profit from market
    1. Risk free **Arbitrage**
        * Location/Latency 
            * Looks at exchanges offering similar prices for same stocks
                * Buying and selling between fragmented markets allows for earning of differences between
        * Triangular
            * Buy and sell pattern in a triangular fashion sometimes don't end up in a 0 net profit.
            * Can take advantage by buying and selling in a circular manner
        * Index
            * Prices are published slow
            * Requires formulaes to be known publicly
            * trades are made in the milliseconds
            * Therefore, makes use of future knowledge to make profits
    2. Non-risk free Arbitrage
        * Statistical
            * ?
        * Pairs Trading
            * Noticing correlations between stocks
            * Takes advantage of x to predict y
        * Mean Reversion
            * Looking at average of stocks
        * Event Driven
            * News driven related to stocks
            * Profits by predicting the impact on market by the news (predicting news ahead of time)
            * Often algos take advantage of this and trade the moment the news comes out
    3. Market timing
        * Fundamental analysis - level of individuals
        * Technical analysis
        * Sentiment Analysis


## Testing the Algo
* Simple testing
    * Backtesting
        * Run using historical data
        * Often used for machine learning
    * Forward Test
        * Run on more recent data
    * Live Test
        * Run on live data
* (*Does not work since*)
    * Backtesting does not affect the market
    * Other algos react
* **IMPORTANT**: Put a kill switch
    * This prevents heavy losses
    * Risk management strategy


## What do exchanges look like today?
* CoLocation services
    * Offers time advantage (micro-seconds vs miliseconds)
    * Also limits the number of calls per second
    * This prevents people from calling API non-stop, which lags it for everyone else
* Time ~0.3ms, which makes it all about latency 
* Current state uses lasers
* Number of orders and trades are in the trillions within the US per day


## Models (Using alternative data)
* Machine Learning
    * GANs
    * Predictive Adaptive Response (Evolutionary ML)
    * Reinforcement Learning
* Game Theory

## Try it out
* Meta Trader 4 (???)

