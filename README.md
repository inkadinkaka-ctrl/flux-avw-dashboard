# flux-avw-dashboard
Volatility-normalized, volume-weighted momentum dashboard for TradingView. Inspired by MACD-V (Alex Spiroglou) but implemented independently with ATR normalization and adaptive volume weighting.
# Flux AVW Dashboard (TradingView Pine Script v6)

**Author:** Ken Anderson  
**License:** MIT  
**Conceptual inspiration:** MACD-V (volatility-normalized MACD) by Alex Spiroglou  

---

## 📘 Overview
The **Flux AVW Dashboard** is an independent, open-source TradingView indicator that visualizes market state through a volatility- and volume-normalized momentum model.  
It extends the idea of MACD-V by introducing **adaptive volume weighting**, **ATR scaling**, and a **dashboard table** summarizing multiple analytics at a glance.

---

## ⚙️ Features
- **Volatility-normalized, volume-weighted momentum core** (AVW MACD / ATR style)  
- **Adaptive EMAs** that adjust to real-time volume and volatility  
- **Trend Slope (Δ ATR)** and **Bias Score (4-system agreement)**  
- **VWAP Δ and CVD proxy** for institutional-flow context  
- **Dynamic table dashboard** with per-bar updates and throttled redraws  
- **Padding and corner placement options** for visual clarity  
- **Fully MIT-licensed and open source**

---

## 🧮 Core Formula (Volatility-Normalized AVW Momentum)

The main momentum engine combines **volume weighting** and **volatility normalization**, making momentum comparable across instruments and timeframes:

\[
\text{Flux AVW Momentum} =
\frac{
  \left[
    \frac{EMA(P \times V, f)}{EMA(V, f)} -
    \frac{EMA(P \times V, s)}{EMA(V, s)}
  \right]
}{
  ATR(n)
}
\]

Where  
- \(P\) = price (close or hlc3)  
- \(V\) = volume  
- \(f, s\) = fast and slow EMA lengths  
- \(ATR(n)\) = average true range for volatility normalization  

_Conceptually inspired by MACD-V (volatility-normalized MACD) by Alex Spiroglou.  
This implementation adds adaptive volume weighting and ATR scaling for real-time responsiveness._

---

## 🧭 Usage
1. Copy the code from `Flux AVW Dashboard.txt` into a new Pine Editor window in TradingView.  
2. Click **Add to Chart**.  
3. Adjust inputs (EMA lengths, ATR period, VWAP Δ bands) as needed.  
4. For publication, include the MIT license header already embedded in the script.

---

## 🪪 License
This project is released under the **MIT License**.  
See the header in `Flux AVW Dashboard.txt` or the [`LICENSE`](LICENSE) file for details.

