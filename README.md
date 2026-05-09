# RRG India — Institutional Capital Rotation Intelligence

Relative Rotation Graph + Capital Rotation Engine for NIFTY 50.

## Latest Rankings (2026-05-08)
| Rank | Symbol | RS | RM | Score | Quadrant |
|------|--------|----|----|-------|----------|
| 1 | BAJAJ-AUTO | 3.55 | 2.87 | 3.2765 | Leading |
| 2 | GRASIM | 3.35 | 2.67 | 3.0753 | Leading |
| 3 | M&M | 1.71 | 3.08 | 2.2566 | Leading |
| 4 | INDUSINDBK | 2.19 | 1.70 | 1.9968 | Leading |
| 5 | APOLLOHOSP | 2.18 | 0.72 | 1.5937 | Leading |
| 6 | DIVISLAB | 2.08 | 0.60 | 1.4866 | Leading |
| 7 | CIPLA | 1.30 | 1.26 | 1.2841 | Leading |
| 8 | ADANIPORTS | 2.42 | -0.49 | 1.2538 | Weakening |
| 9 | ADANIENT | 2.13 | -0.41 | 1.1166 | Weakening |
| 10 | MARUTI | 0.44 | 1.95 | 1.0416 | Leading |
| 11 | SUNPHARMA | 0.99 | 0.82 | 0.9249 | Leading |
| 12 | BAJFINANCE | 1.01 | 0.76 | 0.9071 | Leading |
| 13 | TATASTEEL | 1.37 | 0.13 | 0.8751 | Leading |
| 14 | RELIANCE | 0.78 | 0.82 | 0.7972 | Leading |
| 15 | SHREECEM | 1.39 | -0.14 | 0.7818 | Weakening |
| 16 | ASIANPAINT | 2.44 | -1.79 | 0.7477 | Weakening |
| 17 | JSWSTEEL | 1.65 | -0.85 | 0.6504 | Weakening |
| 18 | NESTLEIND | 2.08 | -1.54 | 0.6333 | Weakening |
| 19 | TATACONSUM | 2.06 | -1.69 | 0.5581 | Weakening |
| 20 | NTPC | 0.95 | -0.27 | 0.4624 | Weakening |
| 21 | ULTRACEMCO | 0.54 | 0.34 | 0.4585 | Leading |
| 22 | TECHM | 0.58 | 0.26 | 0.4512 | Leading |
| 23 | HINDALCO | 1.18 | -0.72 | 0.4186 | Weakening |
| 24 | TITAN | 1.34 | -1.02 | 0.3951 | Weakening |
| 25 | HINDUNILVR | 1.00 | -0.68 | 0.3270 | Weakening |
| 26 | HEROMOTOCO | -0.07 | 0.92 | 0.3262 | Improving |
| 27 | EICHERMOT | 0.12 | 0.64 | 0.3256 | Leading |
| 28 | POWERGRID | 0.60 | -0.31 | 0.2404 | Weakening |
| 29 | COALINDIA | 0.17 | 0.35 | 0.2393 | Leading |
| 30 | DRREDDY | 0.18 | 0.29 | 0.2276 | Leading |
| 31 | UPL | 0.20 | 0.24 | 0.2161 | Leading |
| 32 | KOTAKBANK | -0.47 | 0.95 | 0.0961 | Improving |
| 33 | LT | 0.27 | -0.18 | 0.0881 | Weakening |
| 34 | BAJAJFINSV | -0.17 | 0.28 | 0.0092 | Improving |
| 35 | HDFCLIFE | -0.46 | 0.57 | -0.0477 | Improving |
| 36 | ITC | -0.21 | 0.13 | -0.0739 | Improving |
| 37 | BPCL | -0.69 | 0.53 | -0.2013 | Improving |
| 38 | ONGC | -0.16 | -0.35 | -0.2369 | Lagging |
| 39 | SBILIFE | -0.89 | 0.36 | -0.3912 | Improving |
| 40 | BHARTIARTL | -0.84 | 0.15 | -0.4429 | Improving |
| 41 | HDFCBANK | -1.28 | 0.51 | -0.5598 | Improving |
| 42 | WIPRO | -0.51 | -1.16 | -0.7727 | Lagging |
| 43 | HCLTECH | -1.59 | -0.46 | -1.1390 | Lagging |
| 44 | INFY | -1.49 | -0.79 | -1.2093 | Lagging |
| 45 | AXISBANK | -0.97 | -1.81 | -1.3076 | Lagging |
| 46 | BRITANNIA | -2.28 | -0.14 | -1.4259 | Lagging |
| 47 | ICICIBANK | -1.93 | -2.09 | -1.9945 | Lagging |
| 48 | TCS | -2.14 | -1.83 | -2.0146 | Lagging |
| 49 | SBIN | -2.61 | -1.44 | -2.1445 | Lagging |

## Architecture
- NSE/yfinance OHLCV → parquet pipeline
- Relative Strength (RS) = stock / NIFTY, z-score normalized
- Relative Momentum (RM) = 10-day RS change, EMA smoothed
- Leadership Score = RS×0.6 + RM×0.4
- RRG Quadrants: Leading · Weakening · Lagging · Improving

## Phase Status
- [x] Phase 1: Data pipeline
- [x] Phase 2: RS engine  
- [x] Phase 3: Momentum engine
- [x] Phase 4: RRG visualization
- [x] Phase 5: Ranking engine
- [ ] Phase 6: Dashboard
- [ ] Phase 7: Alerts
- [ ] Phase 8: Institutional features
