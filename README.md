# Correlation across regimes: 2008 versus 2022

Five asset classes, 4,211 daily observations, April 2006 to December 2022.

**The question.** Do correlations converge in a crisis, so that diversification stops working when it is needed most?

**The answer, on this basket.** No. The 2008 crisis window has the lowest average pairwise correlation of the four periods measured. The highest is 2022.

## Results

| Period | Days | Mean pairwise | Equity–bond |
|---|---:|---:|---:|
| Pre-crisis (2006–mid 2007) | 307 | 0.155 | +0.018 |
| Crisis (Sep 2008–Mar 2009) | 146 | **−0.031** | **−0.444** |
| Recovery (2010–2019) | 2,516 | 0.040 | −0.483 |
| **2022** | 251 | **0.251** | **+0.084** |

Equities and long-dated Treasuries moved at −0.44 through the worst of the crisis and stayed near −0.48 for the following decade. The hedge worked. Rolling mean pairwise correlation peaks on 29 December 2022, the most correlated single point in the sample.

### Decomposition

The aggregate was flat across the crisis because two component pairs moved sharply in opposite directions:

| Period | Equity–oil | Equity–gold | Risk-asset mean |
|---|---:|---:|---:|
| Pre-crisis (2006–mid 2007) | +0.082 | +0.246 | +0.259 |
| **Crisis (Sep 2008–Mar 2009)** | **+0.559** | **+0.039** | +0.271 |
| Recovery (2010–2019) | +0.422 | −0.016 | +0.186 |
| 2022 | +0.108 | +0.193 | +0.241 |

Equity–oil rose close to sevenfold. Equity–gold fell to near zero. The mean pairwise figure alone would have missed both.

## Interpretation

The difference between the two episodes is the type of shock, not its severity.

**2008 was a growth shock.** Earnings expectations and oil demand collapsed together; policy rates were cut and investors moved into government paper. Equities and bonds responded in opposite directions, so a balanced portfolio was hedged.

**2022 was a discount-rate shock.** A higher discount rate reduces the present value of company earnings and bond coupons alike, so both legs of the hedge fell through the same channel.

The bond hedge is a property of the kind of shock that arrives, not a property of bonds.

## Limitations

- **No credit exposure.** The basket holds no corporate credit, securitised products or emerging markets, which is where most of the 2008 convergence occurred. The finding concerns these five assets, not the crisis in general.
- **Treasuries benefit from flight to quality**, which makes a negative equity–bond reading in a credit crisis close to inevitable for this basket.
- **Short-dated Treasuries have very low volatility** (0.09% daily standard deviation against 1.27% for equities), which pulls the mean pairwise figure toward zero.
- **Sample starts April 2006**, limited by the oil ETF's inception, leaving about fifteen months of pre-crisis baseline.

## Data

| Asset | Proxy |
|---|---|
| Equities | SPY |
| Long bonds | TLT |
| Short bonds | SHY |
| Gold | GLD |
| Oil | USO |

Prices from Yahoo Finance via `yfinance`, adjusted for splits and dividends. Log returns, 126-day rolling windows.

Note that USO tracks oil futures and carries roll cost, so its returns are not spot oil returns. Adequate for correlation work, not for return attribution.

## Running it

```bash
pip install -r requirements.txt
jupyter notebook correlation-regimes-2008-2022.ipynb
```

Or open the notebook in Colab and run all cells.

## Write-up

[Diversification didn't fail in 2008](https://jackline-jebet.github.io/notes-correlation-breakdown.html)

---

Jackline Jebet · MSc Financial Engineering · [jackline-jebet.github.io](https://jackline-jebet.github.io)
