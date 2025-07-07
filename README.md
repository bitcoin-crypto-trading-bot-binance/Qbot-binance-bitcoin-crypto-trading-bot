Qbot-binance-bitcoin-crypto-trading-bot

Binance bitcoin and crypto automated trading bot.

QBot Automated Bitcoin and Altcoin Trading System.

Project Qultra has developed an advanced software solution designed to automate Bitcoin and altcoin cryptocurrency trading using the Binance API. The system retrieves real-time ticker data, conducts in-depth technical analysis using a unique blended scoring algorithm, generates actionable trading signals (BUY, SELL, or HODL), and automatically executes trades, including setting buy, sell, (stop-loss and take-profit) orders on the exchange.
The primary objective of the QBot Trading System is to enable seamless automated trading using the daily chart timeframe. Analysing Bitcoin, plus multiple altcoin tickers per run with no manual technical analysis required. This allows traders to efficiently capitalise on market opportunities with minimal effort.
System Functionality
The QBot Trading System evaluates market conditions using a suite of widely recognised technical indicators, each contributing to a composite score that informs trading decisions. The indicators include:
Relative Strength Index (RSI): Assesses the magnitude of recent price changes, with specialised logic for extreme overbought or oversold conditions.
Moving Averages (MAs): Compares the latest closing price to 50-day and 200-day moving averages to identify trends.
Bollinger Bands (BBs): Measures price volatility and detects overbought or oversold conditions.
Exponential Moving Averages (EMAs): Analyses the latest closing price against 20-day and 100-day EMAs for trend confirmation.
Moving Average Convergence Divergence (MACD): A trend-following momentum indicator that evaluates the relationship between two moving averages.
Ichimoku Cloud (Ichimoku Kinko Hyo): A comprehensive indicator providing insights into support, resistance, momentum, and trend direction.
Volume and Volatility: Incorporates trading volume and market volatility to enhance decision-making.

Inputs
Latest closing price of the asset.
RSI, Bollinger Bands (upper/lower), MA (50-day, 200-day), EMA (20-day, 100-day), MACD, and Ichimoku Cloud values.
Volume and volatility metrics.
Configurable weights for each indicator in the scoring model.
Capping thresholds for individual and total scores.

Outputs
Individual scores for RSI, MAs, BBs, EMAs, MACD, Ichimoku Cloud, volume, and volatility.
A composite total score representing market sentiment.
Trading signal (BUY, SELL, or HODL) based on predefined thresholds.

Logic
Calculates individual indicator scores using specific formulas and input values.
Detects market state i.e. Bullish, Bearish, Sideways and applies specific weights and thresholds tuned for that state.
Aggregates weighted scores to compute a total score, capping individual and total scores to maintain consistency.
Uses bullish candlestick patterns from the previous close as a confirmation signal.
Generates trading signals and executes trades on the Binance exchange.

Applications
Trading Signal Generation: The composite score drives automated trading decisions, enabling seamless execution of buy, sell, or hold actions.

Risk Management: Indicator scores provide insights into market risk, allowing for dynamic position adjustments.
Portfolio Allocation: Scores guide asset selection, prioritising those with favourable market conditions.

Key Considerations
Weighting: Indicator weights significantly influence the composite score. These are iteratively optimised through genetic algorithms based on back-testing results.
Score Capping: Limits extreme values to ensure a stable scoring range.
Interpretation: Higher scores indicate bullish sentiment, while lower scores suggest bearish conditions. However, traders should consider broader market contexts and external factors as well as technical analysis.

Back-Testing: The system employs historical data to validate strategies, using Python and libraries like DEAP (genetic algorithms), TA-Lib (technical analysis), Pandas, and NumPy (data manipulation).

Back-Testing Framework
The QBot Trading System includes a robust standalone back-testing module to optimise performance and refine trading parameters.
Libraries Utilised
DEAP: Implements genetic algorithms to optimise indicator weights and thresholds.
TA-Lib: Provides technical analysis functions for RSI, MAs, BBs, EMAs, MACD, and Ichimoku Cloud.
Pandas/NumPy: Facilitates efficient data manipulation and analysis.
Multiprocessing: Enables parallel back-testing across multiple tickers for enhanced performance.

Core Components
Back-Testing Function: Retrieves historical ticker data for a specified period.
Applies technical indicators to compute scores and simulate trades.
Evaluates performance metrics, including returns, win rate, Sharpe ratio, and maximum drawdown.

Parallel Back-Testing:
Leverages multiprocessing to concurrently test multiple tickers, significantly reducing computation time.

Summary and Analysis: Aggregates back-test results to provide actionable insights into strategy performance.

Genetic Algorithm Optimisation: Evolves indicator weights and thresholds over multiple generations to maximise returns.
Best-performing parameters are extracted for further refinement or integration with AI-driven analysis.

The QBot Trading System, developed by Project Qultra, is a sophisticated, automated trading solution designed to streamline cryptocurrency trading on the Binance exchange. By combining a unique scoring system, advanced technical indicators, and genetic algorithm optimisation, the system delivers data-driven trading signals with minimal manual intervention. Ongoing back-testing and parameter optimisation ensure the system adapts to evolving market conditions, making it a powerful tool for traders seeking to enhance efficiency and profitability.

I give no warranty and accept no responsibility or liability for the accuracy or the completeness of the information and materials contained in this project. Under no circumstances will I be held responsible or liable in any way for any claims, damages, losses, expenses, costs or liabilities whatsoever (including, without limitation, any direct or indirect damages for loss of profits, business interruption or loss of information) resulting from or arising directly or indirectly from your use of or inability to use this code or any code linked to it, or from your reliance on the information and material on this code, even if I have been advised of the possibility of such damages in advance.