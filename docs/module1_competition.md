---
title: Market Competition Indicators
layout: default
---

# Market Competition Indicators (Module 1 – Concentration Measures)

> This page summarizes the indicators used to assess market concentration, with formulas and quick interpretations.  
> Notation: firm $i \in \mathcal{N}$, sector $j \in \mathcal{J}$, period $t \in \mathcal{T}$.

---

## 1) Revenue Market Share

**Definition.** Share of firm $i$’s revenue in sector $j$ at time $t$.

$$
s_{ijt} \equiv \text{MarketShare}_{ijt}
= \frac{\text{revenue}_{ijt}}{\sum_{i \in j} \text{revenue}_{ijt}}
$$

**Use:** Analyze distribution of firm sizes (mean, median, dispersion).

---

## 2) Adjusted Revenue Market Share (Trade-Adjusted)

**Goal.** Focus on **domestic** market position by removing exports from the firm and using **sector domestic absorption** (output + imports − exports) as the denominator.

$$
s^{\text{adj}}_{ijt}
= \frac{\text{revenue}_{ijt} - \text{export}_{ijt}}
{\sum_{i \in j} \text{revenue}_{ijt} + \text{import}_{jt} - \text{export}_{jt}}
$$

This can be written as a **sector-time scalar** times the unadjusted share:

$$
s^{\text{adj}}_{ijt}
= \hat{\alpha}_{jt} \, s_{ijt},
\quad
\hat{\alpha}_{jt}
= \frac{\sum_{i \in j} \text{revenue}_{ijt}}
{\sum_{i \in j} \text{revenue}_{ijt} + \text{import}_{jt} - \text{export}_{jt}}
$$

**Use:** Better measure of local (domestic) competitive position when trade is material.

---

## 3) Herfindahl–Hirschman Index (HHI)

**Definition.** Sum of squared market shares (0–1 scale if shares are in proportions).

$$
HHI_{jt} = \sum_{i \in j} s_{ijt}^{\,2}
$$

**Trade-adjusted HHI.** Using the relation $s^{\text{adj}}_{ijt} = \hat{\alpha}_{jt} s_{ijt}$:

$$
HHI^{\text{adj}}_{jt}
= \sum_{i \in j} \left(s^{\text{adj}}_{ijt}\right)^2
= \hat{\alpha}_{jt}^{\,2}\, \sum_{i \in j} s_{ijt}^{\,2}
= \hat{\alpha}_{jt}^{\,2} \, HHI_{jt}
$$

**Interpretation:** Higher $HHI$ → more concentrated market.

---

## 4) HHI Decomposition (Inequality vs. Number of Firms)

**Idea.** Separate concentration into:
- **Size inequality effect** $E^i_{jt}$, and
- **Number of firms effect** $E^n_{jt}$.

$$
HHI_{jt} = E^i_{jt} + E^n_{jt}, 
\qquad
E^i_{jt} = \tau^2_{jt},
\quad
E^n_{jt} = HHI_{jt} - \tau^2_{jt}
$$

Where a common definition is:

$$
\tau^2_{jt} = \frac{n_{jt} \cdot HHI_{jt} - 1}{n_{jt} - 1},
$$

with $n_{jt}$ = number of operating firms in sector $j$ at time $t$.

**Interpretation:** Tells whether concentration is driven by **unequal sizes** or by **few firms**.

---

## 5) Concentration Ratio $CR_K$ (e.g., CR4, CR8)

**Definition.** Sum of market shares of the **top $K$** firms.

$$
CR_{K, jt} = \sum_{k=1}^{K} s_{(k)jt}
$$

where $s_{(k)jt}$ is the $k$-th largest market share in $(j,t)$.

**Interpretation:** Higher $CR_K$ → dominance by a few leaders (oligopoly signal).

---

## 6) Share of Top Percentiles (Top 1%, 10%, 25%)

**Definition.** Aggregate share of firms in the **top $K\%$** of the size distribution.

$$
\text{Share Top }K\%_{jt} = \sum_{i \in \text{Top }K\%} s_{ijt}
$$

**Interpretation:** Higher value → stronger dominance by the head of the distribution.

---

## 7) Share of Bottom 50%

**Definition.** Aggregate share of the **smallest half** of firms.

$$
\text{Share Bottom 50\%}_{jt} = \sum_{i \in \text{Bottom }50\%} s_{ijt}
$$

**Interpretation:** Higher value → broader competitive base; lower → dominance of large firms.
---

## 8) Dominance Index (DI)

**Definition.** Sum of squared **adjacent gaps** in ranked market shares (descending).

$$
DI_{jt} = \sum_{i=1}^{N_{jt}-1} \left(s_{(i)jt} - s_{(i+1)jt}\right)^2
$$

**Interpretation:** Higher $DI$ → large gaps between leaders and followers (strong dominance).

---

## Quick Interpretation Cheatsheet

- **High $HHI$, $CR_K$, Top% share, or $DI$:**
  → **More concentrated**; few firms dominate.

- **High Bottom 50% share, low $DI$:**
  → **More competitive**; size distribution more even.

- **Trade-adjusted measures:**
  → Emphasize **domestic** competition by removing export effects and accounting for imports.

---

## Practical Notes

- Use **shares as proportions** (0–1) for consistency across indicators.  
- For time series, compute indicators at each $t$ and analyze trends and breaks.  
- When trade is important, prefer **adjusted** measures alongside unadjusted ones.
