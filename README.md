Trend Target 

Attempting to mathematically replicate uptrends and downtrends to use as a target in a machine learning model.
Warning: This is not a trading indicator and should not be used for live trading, as it contains lookahead bias. Its purpose is solely for training ML models.

How it works

Peak and Trough Detection

Selects the highest high and lowest low within a given lookback window.

Line Interpolation

Connects the peaks and troughs with interpolated lines.

Facilitates trend movement visualization.

Target Calculation

Computes the percentage change between consecutive peaks and troughs.

Assigns the target:

Uptrend (1): if both percentage changes exceed threshold_pct.

Downtrend (-1): if both percentage changes are below -threshold_pct.

Neutral (0): otherwise.
