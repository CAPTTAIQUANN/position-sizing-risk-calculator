# Automated Position-Sizing & Risk-Exposure Calculator (Excel & Python)

## Project Overview
A universal position-sizing and risk-management model built in both **Microsoft Excel** and **Python** to standardize capital-at-risk across Crypto Perpetual Futures and Forex markets. Instead of entering arbitrary position sizes, this tool calculates the exact unit quantity, USDT order value, or FX lot size required so that any trade hitting its Stop-Loss loses strictly the predefined dollar risk amount.

## Core Formula & Logic
Regardless of asset price or volatility, the model enforces fixed-dollar risk using a universal two-step calculation:
1. **Unit / Coin Quantity:** `Risk ($) / |Entry Price - Stop Loss Price|`
2. **Total Order Value (USDT):** `Unit Quantity × Entry Price`
3. **FX Standard Lots:** `Unit Quantity / 100,000`

### Example Calculation (Included in Excel & Python Models)
* **Entry Price (E):** `0.87718`
* **Stop Loss (SL):** `0.87678` (Stop distance = `0.00040`)
* **Fixed Dollar Risk:** `$100.00`
* **Calculated Unit Size:** `250,000 units`
* **Output Order Value:** `$219,295 USDT`
* **Automated 1:3 R:R Take-Profit Target:** `0.87838`

## Files in This Repository
* `Position_Size_Calculator.xlsx` — Interactive Excel calculator for rapid pre-trade order value sizing.
* `Universal_Position_Size_Calculator.ipynb` — Python script that automates Long/Short direction detection, 1:3 Risk-Reward Take-Profit projection, and dual Crypto/Forex sizing.
