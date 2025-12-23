# 🚀 Multi-Asset Crypto Trading System (Phase 3)

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Sharpe](https://img.shields.io/badge/Sharpe-0.96-success.svg)]()
[![Status](https://img.shields.io/badge/Status-Phase%203%20Complete-success.svg)]()

> **A hybrid machine learning and momentum-based cryptocurrency trading system that achieved 0.96 Sharpe ratio with 48% lower drawdown than buy-and-hold, demonstrating the value of asset-specific strategy design and rigorous risk management.**

## 📊 Performance Results (2020-2025 Backtest)

```
📈 Total Return:       612%    (26% annualized)
⚡ Sharpe Ratio:       0.96    (near institutional grade)
📉 Max Drawdown:       -37%    (vs -70% buy & hold)
🎯 Win Rate:           53%     (positive edge)
💰 Portfolio:          70% BTC / 30% ETH
```

**Key Insight**: *Prioritized risk-adjusted returns over maximum gains. Lower peak returns in exchange for significantly better Sharpe ratio and reduced drawdowns.*

![Dashboard](results/phase3_v64_dashboard.png)

---

## 🎯 What This Project Demonstrates

### The Problem
Most crypto systems fail because they:
- Apply one strategy to all assets (ignoring characteristics)
- Optimize for maximum returns (ignoring risk)
- Hide failures (only show winning results)

### My Approach
Built an **asset-specific risk-managed system** that:

1. **🤖 Machine Learning for BTC**
   - Stable asset → ML predictions reliable
   - Result: 818% return, 0.90 Sharpe, 51% win rate

2. **📈 Momentum+ML for ETH** 
   - Volatile asset → Momentum captures explosive moves
   - Result: 165% return, 0.62 Sharpe, 58% win rate

3. **⚖️ Smart Portfolio Construction**
   - Sortino-based allocation (downside risk focus)
   - Result: 0.96 Sharpe, -37% max drawdown

4. **📝 Honest Documentation**
   - Tested XRP → Failed (-86% return)
   - Documented WHY it failed
   - Excluded from final system

**Trade-off Accepted**: Underperformed buy-and-hold by 1373% in total returns, but achieved 0.96 Sharpe vs 0.82 B&H and -37% drawdown vs -70% B&H.

---

## 🏗️ System Architecture

```
┌────────────────────────────────────────────────────────┐
│              ASSET CHARACTERIZATION                    │
│                                                        │
│  BTC: Stable, Predictable    ETH: Explosive, Trends   │
│  → Use ML Predictions        → Use Momentum Signals   │
└────────────────────────────────────────────────────────┘
                        ↓
┌────────────────────────────────────────────────────────┐
│            STRATEGY IMPLEMENTATION                     │
│                                                        │
│  BTC Strategy              ETH Strategy               │
│  • Ensemble ML             • Triple momentum check    │
│  • Regime thresholds       • ML confirmation          │
│  • SMA100 filter           • Extreme filters          │
│  • 59% exposure            • 11% exposure             │
│  • 72 trades (low cost)    • 162 trades (selective)   │
└────────────────────────────────────────────────────────┘
                        ↓
┌────────────────────────────────────────────────────────┐
│         RISK-MANAGED ALLOCATION                        │
│                                                        │
│  Sortino Optimization → 70% BTC / 30% ETH            │
│  Result: 0.96 Sharpe, -37% Max DD                     │
└────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/yourusername/crypto-trading-phase3.git
cd crypto-trading-phase3
pip install -r requirements.txt
```

### Run Backtest
```bash
python trading_system_v64.py
```

### Expected Output
```
BTC-USD: 818% return, 0.90 Sharpe, 72 trades
ETH-USD: 165% return, 0.62 Sharpe, 162 trades
Portfolio: 612% return, 0.96 Sharpe, -37% DD

✅ Both assets profitable
✅ Sharpe near institutional grade
✅ Significantly lower drawdown than buy-and-hold
```

---

## 📈 Detailed Results

### Portfolio-Level Metrics

| Metric | Strategy | 50/50 B&H | Comparison |
|--------|----------|-----------|------------|
| **Total Return** | 612% | 1,768% | -65% underperform |
| **Sharpe Ratio** | **0.96** | 0.82 | **+17% better** |
| **Sortino Ratio** | 1.49 | 1.12 | **+33% better** |
| **Max Drawdown** | **-37%** | -70% | **+47% better** |
| **Calmar Ratio** | 0.69 | 0.52 | **+33% better** |
| **Win Rate** | 53% | N/A | Positive edge |

**Value Proposition**: Accept lower returns for significantly better risk metrics (Sharpe, drawdowns, consistency).

### Asset-Level Performance

#### BTC-USD (ML-Driven)
```
Strategy:       Machine Learning + Trend Filter
Training:       2017-2019 (1,092 samples)
Testing:        2020-2025 (2,168 days)

Results:
├─ Return:      818% (vs 1,162% B&H)
├─ Sharpe:      0.90 (solid)
├─ Trades:      72 (efficient)
├─ Win Rate:    51% (edge confirmed)
├─ Exposure:    59% (selective entry)
└─ Cost Drag:   10% (low frequency advantage)

Assessment: ✅ Conservative capital preservation approach
```

#### ETH-USD (Momentum+ML)
```
Strategy:       Momentum + ML Confirmation
Training:       2018-2019 (583 samples)
Testing:        2020-2025 (2,168 days)

Results:
├─ Return:      165% (vs 2,375% B&H)
├─ Sharpe:      0.62 (acceptable)
├─ Trades:      162 (moderate frequency)
├─ Win Rate:    58% (strong hit rate)
├─ Exposure:    11% (highly selective)
└─ Cost Drag:   22% (trade-off for selectivity)

Assessment: ⚠️ Missed peak euphoria, but maintained discipline
```

---

## 🔬 Development Journey (V6.0 → V6.4)

This wasn't a one-shot success. Here's the real story:

### V6.0: Initial Attempt (FAILED)
```
Approach: Apply same ML strategy to all assets
Result:   
  • ETH: Only 32 trades, -23% return
  • XRP: Only 20 trades, -75% return
Learning: One-size-fits-all doesn't work
```

### V6.1-V6.2: Discovery Phase
```
Found:    ML confidence too low for altcoins
          ETH max prob: 0.509 (barely above 0.5)
Learning: Need momentum as primary, ML as secondary
```

### V6.3: Hybrid Success (But Overtrade)
```
Result:   ETH: 1,293% return! But 205 trades
          XRP: -86% (disaster)
Learning: Momentum works, but need optimization
          Some assets not suitable at all
```

### V6.4: Final Production (BALANCED)
```
Changes:  • Removed XRP (documented failure)
          • Added strict signal persistence
          • Optimized for risk, not returns
          
Result:   ✅ 0.96 Sharpe (near institutional)
          ✅ -37% DD (vs -70% B&H)
          ✅ Both assets profitable
          ⚠️ Lower returns (risk trade-off accepted)
```

**Key Learning**: Better to have **realistic results with honest analysis** than inflated numbers with hidden problems.

---

## 💡 Why Different Strategies?

### BTC Works with ML Because:
```
✓ Long history (2009+) = 15+ years training data
✓ Lower volatility (ATR ~5%) = predictable patterns
✓ Market leader = drives price action, less manipulated
✓ High ML confidence (probs 0.44-0.71) = reliable signals

Result: 818% return, 0.90 Sharpe, 72 efficient trades
```

### ETH Needs Momentum Because:
```
✓ Explosive moves (10-30% daily) = catch trends early
✓ Clear trend phases = momentum alignment works
✓ ML trained on bear (2018-2019) = too pessimistic for bull
✓ Low ML confidence (max 0.494) = can't rely on predictions alone

Solution: Use momentum PRIMARY, ML as veto (confirmation only)
Result: 165% return, 0.62 Sharpe, 58% win rate
```

### XRP Failed Because:
```
✗ Extreme volatility (ATR 8-12%) = constant whipsaws
✗ Different cycle timing = peaks April vs Nov (misaligned)
✗ Fundamental driven = SEC lawsuit matters more than technicals
✗ Lower liquidity = higher slippage impacts performance

Result: -86% return, -0.28 Sharpe, 380 overtrades
Decision: Excluded from production system
```

**Takeaway**: Not every asset benefits from systematic trading. Asset selection is as important as strategy design.

---

## 🎯 Phase 3 Objectives ✅ COMPLETE

### Extended Validation ✅
- [x] 5+ years backtesting (2020-2025)
- [x] COVID crash, bull run, bear market
- [x] 72-162 trades per asset (statistical significance)
- [x] Out-of-sample testing (no look-ahead bias)



### Multi-Asset Extension ✅
- [x] Tested 3 assets (BTC, ETH, XRP)
- [x] Asset-specific models and strategies
- [x] Portfolio optimization (Sortino-based)
- [x] Result: 70/30 BTC/ETH allocation

### Risk Management ✅
- [x] Cost efficiency analysis (10-22% drag)
- [x] Signal persistence (reduce whipsaw)
- [x] Drawdown control (-37% vs -70%)
- [x] Diversification constraints (30-70%)

**Status**: ✅ **ALL OBJECTIVES MET**

---

## 🧠 Key Learnings

### Technical Insights
1. **ML confidence threshold matters**
   - BTC: max prob 0.71 → ML useful
   - ETH: max prob 0.49 → ML limited, use as filter only

2. **Signal persistence crucial**
   - Without: 205 trades, 26% cost drag
   - With: 162 trades, 22% cost drag (still selective)

3. **Risk-adjusted > absolute returns**
   - 612% return but 0.96 Sharpe = better than
   - 1,768% return but 0.82 Sharpe

### Strategy Insights
1. **Asset-specific beats one-size-fits-all**
   - Tried same strategy → failed
   - Customized per asset → success

2. **Momentum + ML hybrid effective**
   - Pure ML: too low confidence
   - Pure momentum: too many signals
   - Hybrid: best of both worlds

3. **Not all assets tradeable**
   - XRP: -86% return documented
   - Better to exclude than force fit

### Professional Insights
1. **Document failures honestly**
   - Shows critical thinking
   - Demonstrates learning process
   - More credible than perfect results

2. **Risk management matters**
   - Lower returns acceptable
   - If Sharpe and DD significantly better

3. **Iteration beats perfection**
   - 5 versions to get here
   - Each taught something valuable

---

## 🗺️ Phase 4 Roadmap

Building on Phase 3 learnings:

### 1. ETH Strategy Redesign
### 2. Dynamic Position Sizing (Professional Upgrade)
### 3. Portfolio-Level Risk Controls (Hedge Fund Standard)
### 4. Walk-Forward Validation (Robustness Proof)
### 5. Selective Asset Expansion (2–3 Assets Only)
### 6. (Optional) AutoGluon Benchmarking
**Timeline**: Q1 2026

---

## 🛠️ Technical Stack

```
Language: Python 3.9+

Data & Analysis:
  pandas, numpy       (data processing)
  yfinance            (crypto data)
  TA-Lib              (technical indicators)

Machine Learning:
  scikit-learn        (RandomForest, GradientBoosting)
  Stacking ensemble   (5-fold CV)
  StandardScaler      (feature normalization)

Visualization:
  matplotlib, seaborn (charts & dashboards)
```

---

## 📚 Project Structure

```
Phase3/
├── README.md                    # This file
├── trading_system_v64.py        # Main system (800+ lines)
├── DOCUMENTATION.md             # Complete analysis (160+ pages)
├── requirements.txt             # Dependencies
├── results/
│   ├── backtest_results.csv    # Trade history
│   └── dashboard.png            # Performance visualization
└── docs/
    ├── development_journey.md   # V6.0 → V6.4 evolution
    ├── why_btc_ml_works.md      # ML success analysis
    ├── why_eth_needs_momentum.md # Momentum rationale
    └── why_xrp_failed.md        # Failure case study
```

---

## ⚠️ Important Disclaimers

### Risk Warnings
```
⚠️ Past performance does NOT guarantee future results
⚠️ Cryptocurrency trading is EXTREMELY RISKY
⚠️ You can LOSE ALL invested capital
⚠️ This is NOT financial advice
⚠️ System underperformed buy-and-hold in absolute returns
```

### Honest Assessment
```
This system PRIORITIZES:
✓ Risk-adjusted returns (Sharpe ratio)
✓ Capital preservation (lower drawdowns)
✓ Consistency (positive win rate)

This system DOES NOT:
✗ Maximize absolute returns
✗ Beat buy-and-hold in bull markets
✗ Guarantee profits

Trade-off: Accept lower returns for better risk metrics
```

### Recommendations
```
✓ Paper trade minimum 2-3 months
✓ Start with small capital (<5% portfolio)
✓ Understand code completely before using
✓ Monitor performance continuously
✓ Set stop-loss limits
✓ Don't risk money you can't afford to lose
```

---

## 🤝 Contributing

Contributions welcome! Areas for improvement:

- [ ] Reduce ETH signal persistence (increase exposure)
- [ ] Test additional assets (SOL, AVAX, LINK)
- [ ] Implement dynamic position sizing
- [ ] Add real-time monitoring dashboard
- [ ] Create paper trading module

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📞 Contact

**Author**: DEWA  
**Date**: December 13, 2025  
**Status**: Phase 3 Complete ✅

**Links**:
- GitHub: [github.com/whard2205]
- LinkedIn: [https://www.linkedin.com/in/suja-dewa-6326b130b/]
- Instagram: cryptoniac.id , qu.4tf_ 
- Email: syujadewakusuma@gmail.com

---

## 📜 License

MIT License - See [LICENSE](LICENSE) file

Free to use, modify, and distribute. Attribution appreciated.

---

## 🙏 Acknowledgments

- Yahoo Finance (data source)
- scikit-learn, TA-Lib (libraries)
- Renaissance Technologies, AQR (inspiration)

---

## 📈 Results Summary

```
✅ Built asset-specific multi-strategy system
✅ Achieved 0.96 Sharpe (near institutional grade)
✅ Reduced drawdown 47% vs buy-and-hold
✅ Documented complete development journey
✅ Included honest failure analysis (XRP)
✅ All Phase 3 objectives completed

⚠️ Underperformed B&H in absolute returns
   Trade-off accepted for better risk metrics
   
🚀 Ready for Phase 4: Adaptive framework
```

---

**Phase 3 Status**: ✅ **COMPLETE**  
**Next**: Phase 4 Development 

---

*"It's not about having the highest returns. It's about having the best risk-adjusted returns you can trust."*
