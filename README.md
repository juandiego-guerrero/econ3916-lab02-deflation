# econ3916-lab02-deflation
# Deflating Economic Data — Nominal vs. Real

## Objective
This project converts nominal U.S. wage and price data into constant 2020 dollars
using the Consumer Price Index, isolating changes in real purchasing power from the
effects of general inflation.

## Methodology
- **Data acquisition:** Retrieved the Consumer Price Index (CPI) and Average Hourly
  Earnings series directly from the Federal Reserve Economic Data (FRED) database
  through its public CSV endpoint, removing the need for API authentication and
  keeping the pipeline fully reproducible.
- **Deflation function:** Implemented a reusable `deflate_series()` function that
  rebases CPI to a chosen reference year and rescales any nominal series into
  constant dollars using the ratio of base-year CPI to period CPI.
- **Wage analysis:** Applied the function to average hourly earnings to express
  wages in constant 2020 dollars, allowing a direct comparison of nominal and real
  wage trajectories over the sample period.
- **Price case study:** Deflated the U.S. Big Mac price over the same window and
  compared its nominal growth, real growth, and cumulative CPI inflation to test
  whether the product's price outpaced or trailed the general price level.
- **Interactive explorer:** Built an interactive deflation tool with a base-year
  slider, demonstrating that the choice of reference year changes the level of real
  values but leaves their relative movements unchanged.

## Key Findings
- **Nominal vs. real wages:** Nominal average hourly earnings rose from
  $[YOUR VALUE] to $[YOUR VALUE], while real earnings in 2020 dollars moved from
  $[YOUR VALUE] to $[YOUR VALUE]. Much of the apparent nominal gain reflects
  inflation rather than an increase in purchasing power.
- **Big Mac pricing:** The U.S. Big Mac price increased [YOUR VALUE]% in nominal
  terms and [YOUR VALUE]% in real terms, compared with cumulative CPI inflation of
  [YOUR VALUE]% over the same dates. This indicates that the Big Mac's price
  [outpaced / roughly tracked / lagged] the overall price level.
- **Base-year invariance:** The interactive explorer confirms that rebasing shifts
  real dollar levels without altering growth rates, which reinforces that
  conclusions about real trends do not depend on the reference year chosen.

## Tools
Python, pandas, FRED public data, interactive widgets (Google Colab)
