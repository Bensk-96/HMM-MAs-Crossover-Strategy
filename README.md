# HMM-MAs-Crossover-Strategy

Trade SPY

Strategy 1 : SMAs crossover
Long position when fast SMA > slow SMA in bull regime
Close position slow SMA crosses fast SMA from below or in bear regime

Ref : https://www.quantstart.com/articles/market-regime-detection-using-hidden-markov-models-in-qstrader/

Strategy 2 : 4 SMAs crossover
Modification of https://kernc.github.io/backtesting.py/doc/examples/Parameter%20Heatmap%20&%20Optimization.html
Long position when close price crosses sma_enter in 1) bull regime and 2) fast SMA > slow SMA
Close position when 1) sma_enter crosses close price from below, 2) sma_exit crosses close price from below or 3) in bear regime

Strategy 3 : Kalman Filter - SMA crossover
Long position when Kalman filter of close > SMA in bull regime
Close position if SMA cross Kalman Filter or in bear regime

Assume no comission, e.g. Alpaca
#3 x leverage

Grid Search Parameters from 2013 to 2017

