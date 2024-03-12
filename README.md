Trade SPY with Advanced SMA Strategies (Bull Regime Focused)

Overview: Utilizing Hidden Markov Models (HMM) to identify bull regimes (less volatile market phases), this repository features three distinct SMA-based trading strategies on SPY. The strategies are activated during these identified bull regimes to optimize performance.

- Strategy 1: Standard SMA Crossover

Long Position: Initiate when the fast SMA exceeds the slow SMA in a bull regime.
Close Position: Exit when the slow SMA crosses below the fast SMA or if a bear regime begins.
Reference: Market Regime Detection with HMM 
https://www.quantstart.com/articles/market-regime-detection-using-hidden-markov-models-in-qstrader/


- Strategy 2: Enhanced 4-SMA Crossover

Long Position: Enter when the close price is above sma_enter, and the fast SMA is above the slow SMA, exclusively in a bull regime.
Close Position: Exit upon sma_enter falling below the close price, sma_exit falling below the close price, or a transition to a bear regime.
Inspired by Parameter Heatmap & Optimization
https://kernc.github.io/backtesting.py/doc/examples/Parameter%20Heatmap%20&%20Optimization.html


- Strategy 3: Kalman Filter-SMA Integration

Long Position: Initiate when the Kalman filter of the close price surpasses the SMA during a bull regime.
Close Position: Exit when the SMA crosses below the Kalman Filter or upon a shift to a bear regime.
Experimental Setup

No Commission (e.g., Alpaca Broker)
Leverage: 3x
Parameter Grid Search: 2013-2017
Additional Information

For detailed backtest visualization, open the provided Notebook on Google Colab.

Note : Open the Notebook on Google Colab to check the backtest visualization

