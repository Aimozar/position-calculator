# 仓位计算器 — Position Calculator

A lightweight, single-page trading position-size calculator. No dependencies, no build step — just open `index.html` in any browser.

## Features

- **做多 / 做空** direction toggle (Long / Short)
- Account balance & per-trade risk % (with slider)
- Entry price, stop-loss price, take-profit price
- Leverage multiplier support (spot to 125×)
- Calculates:
  - **Position size** (units)
  - **Position value** and required margin
  - **Max risk $** and stop-loss distance %
  - **Expected profit** and **R:R ratio** (when target is set)
  - **Account % used**

## Usage

```
open index.html
```

Fill in your account balance, desired risk %, entry price, and stop-loss price.  
The results update instantly as you type.

## Formula

```
Risk Amount   = Account Balance × Risk %
Position Size = Risk Amount / |Entry − Stop Loss|
Position Value = Position Size × Entry Price
Margin Used    = Position Value / Leverage
R:R Ratio      = Expected Profit / Risk Amount
```