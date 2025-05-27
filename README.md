# Hidden Markov Model Enhanced SMA Strategies

Overview: Utilizing Hidden Markov Models (HMM) to identify different regimes, this repository features three distinct SMA-based trading strategies on SPY. The strategies are activated during these identified bull regimes to optimize performance.

Note: For correct rendering, please clone this repository and open the .ipynb notebook locally in Jupyter or VS Code.

## Strategy 1: Standard SMA Crossover

- Long Position: Initiate when the fast SMA exceeds the slow SMA in a bull regime.
- Close Position: Exit when the slow SMA crosses below the fast SMA or if a bear regime begins.
- Reference: [Market Regime Detection with HMM](https://www.quantstart.com/articles/market-regime-detection-using-hidden-markov-models-in-qstrader/)
 
## Strategy 2: Enhanced 4-SMA Crossover

- Long Position: Enter when the close price is above sma_enter, and the fast SMA is above the slow SMA, exclusively in a bull regime.
- Close Position: Exit upon sma_enter falling below the close price, sma_exit falling below the close price, or a transition to a bear regime.
- Reference: https://kernc.github.io/backtesting.py/doc/examples/Parameter%20Heatmap%20&%20Optimization.html
 
## Strategy 3: Kalman Filter-SMA Integration

- Long Position: Initiate when the Kalman filter of the close price surpasses the SMA during a bull regime.
- Close Position: Exit when the SMA crosses below the Kalman Filter or upon a shift to a bear regime.

## Setup
No Commission (e.g., Alpaca Broker)

Leverage: 3x

Parameter Grid Search: 2013-2017

For detailed backtest visualization, open the provided Notebook on Google Colab.


## Result
![image](https://github.com/Bensk-96/HMM-MAs-Crossover-Strategy/assets/91371262/05117633-4020-4da4-9155-35fda3710bbb)

- Sharpe Ratio
Sharpe Ratio of Benchmark(SPY) : 0.622

Sharpe Ratio of Strategy 1 : 0.670

Sharpe Ratio of Strategy 2 : 0.930

Sharpe Ratio of Strategy 3 : 0.657

- Maximum Drawdown
MDD of Benchmark(SPY) : 0.341

MDD of Strategy 1 : 0.324

MDD of Strategy 2 : 0.248

MDD of Strategy 3 : 0.326

## Next Steps
- Paper Trading and Live Trading
