# Trend Target (for ML training only)

**Attempting to mathematically replicate uptrends and downtrends to use as a target in a machine learning model.**
**Warning:** This is **not a trading indicator** and **should not be used for live trading**, as it contains lookahead bias. Its purpose is **solely for training ML models**.

## How it works

1. **Peak and Trough Detection**

   * Selects the **highest high** and **lowest low** within a given lookback window.

2. **Line Interpolation**

   * Connects the peaks and troughs with interpolated lines.
   * Facilitates trend movement visualization.

3. **Target Calculation**

   * Computes the **percentage change** between consecutive peaks and troughs.
   * Assigns the target:

     * **Uptrend (1):** if both percentage changes exceed `threshold_pct`.
     * **Downtrend (-1):** if both percentage changes are below `-threshold_pct`.
     * **Neutral (0):** otherwise.

## Example Usage

* Visualize the price line with detected peaks and troughs.
* Generate interpolated lines for trend representation.
* Compute targets for machine learning models.


https://github.com/rodrigopaixaosilveira/trend_target/blob/main/output.png
