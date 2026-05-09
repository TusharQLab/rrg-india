# RRG India — Institutional Capital Rotation Intelligence

Relative Rotation Graph + Capital Rotation Engine for NIFTY 50.

## Sector Snapshot (2026-05-08)
| Sector | RS | RM | Score | Quadrant |
|--------|----|----|-------|----------|
| Auto | 1.15 | 1.89 | 1.4453 | Leading |
| Infra | 1.68 | 0.30 | 1.1290 | Leading |
| Pharma | 1.35 | 0.74 | 1.1034 | Leading |
| Metals | 1.40 | -0.48 | 0.6480 | Weakening |
| Consumer | 0.79 | -0.61 | 0.2290 | Weakening |
| Energy | 0.27 | 0.13 | 0.2168 | Leading |
| FMCG | 0.53 | -0.78 | 0.0038 | Weakening |
| Financial | -0.56 | -0.02 | -0.3436 | Lagging |
| IT | -1.03 | -0.80 | -0.9369 | Lagging |

## Stock Rankings — Top 10 (2026-05-08)
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

## Architecture
- yfinance OHLCV → parquet pipeline
- RS = stock / NIFTY index, z-score normalized
- RM = 10-day RS change, EMA smoothed  
- Score = RS×0.6 + RM×0.4
- Sector RRG = equal-weighted RS/RM per sector

## Phase Status
- [x] Phase 1: Data pipeline
- [x] Phase 2: RS engine
- [x] Phase 3: Momentum engine
- [x] Phase 4: RRG visualization
- [x] Phase 5: Stock ranking engine
- [x] Phase 6: Sector RRG
- [ ] Phase 7: Dashboard
- [ ] Phase 8: Alerts
