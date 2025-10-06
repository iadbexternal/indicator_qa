---
title: "Module 2 – Firm Dynamism Indicators"
layout: default
---

# Module 2 – Firm Dynamism Indicators

> These indicators measure **how dynamic and competitive** markets are over time, based on firm entries, exits, rank changes, and job flows.  
> A dynamic market shows **high turnover at the top**, **frequent reshuffling**, and **strong job creation/destruction**, indicating innovation and competition.

---
## 1. Turnover at the Top

**Definition.** Measures the probability that a firm in the **top 4** leaves the top group after _k_ years.

$$
\text{Turnover}_{jt} =
\frac{N_{\text{exiters},\,j,\,t\to t+k}}{N_{\text{firms},\,j,t}^{\text{top 4}}}
$$

Or equivalently,

$$
\text{Turnover}_{jt} =
\Pr\!\Big(
\text{MktSh}_{i,j,t+k} < \text{MktSh}^{(4)}_{j,t+k}
\;\big|\;
\text{MktSh}_{i,j,t} \ge \text{MktSh}^{(4)}_{j,t}
\Big)
$$

**Interpretation:**  
High values → frequent leadership changes (**dynamic market**).  
Low values → stable market (**less competition**).

---

## 3. Entry Rate

**Definition.** Share of firms that **enter** a sector in _t_.

$$
\text{EntryRate}_{jt} =
\frac{N_{\text{entrants},\,jt}}{N_{\text{producing firms},\,jt}}
$$

---

## 4. Exit Rate

**Definition.** Share of firms that **exit** the market in _t_.

$$
\text{ExitRate}_{jt} =
\frac{N_{\text{exiters},\,jt}}{N_{\text{producing firms},\,jt}}
$$
**Interpretation:**  
High → low barriers and strong business creation.  
Low → stagnation or high barriers.

---

## 4. Exit Rate

**Definition.** Share of firms that **exit** the market in _t_.

$$
\text{ExitRate}_{jt} =
\frac{\text{\# exiters}_{jt}}{\text{\# producing firms}_{jt}}
$$

**Interpretation:**  
High → intense competition or sector decline.  
Low → stability.

---

## 5. Establishment Size

Average employment between _t_ and _t − 1_ for firm _i_:

$$
x_{it} =
\frac{\text{employment}_{it} + \text{employment}_{i,t-1}}{2}
$$

Sector-level or national aggregates:

$$
X_t = \sum_{j\in J}\sum_{i\in j} x_{it}
$$

---

## 6. Employment Growth Rate

**Definition.**

$$
g_{it} =
\frac{\text{employment}_{it} - \text{employment}_{i,t-1}}{x_{it}}
$$

Ranges ∈ [−2,+2]; −2 = exit, +2 = entry.  

Aggregate to sector _j_:

$$
g_{jt} =
\sum_{i\in j}
\frac{x_{it}}{X_{jt}}\,g_{it}
$$

---

## 7. (Gross) Job Creation Rate

$$
POS_{jt} =
\sum_{i\in j,\,g_{it}>0}
\frac{x_{it}}{X_{jt}}\,g_{it}
$$

Decompose:

$$
POS_{jt} = POS_{\text{Entry},jt} + POS_{\text{Cont},jt}
$$

- **Entry:** new firms (\(g_{it}=2\))  
- **Continuing:** existing firms (\(0<g_{it}<2\))

---

## 8. (Gross) Job Destruction Rate

$$
NEG_{jt} =
\sum_{i\in j,\,g_{it}<0}
\frac{x_{it}}{X_{jt}}\,|g_{it}|
$$

Decompose:

$$
NEG_{jt} = NEG_{\text{Exit},jt} + NEG_{\text{Cont},jt}
$$

- **Exit:** \(g_{it}=-2\) (firm closure)  
- **Continuing:** \(-2<g_{it}<0\)

---

## 9. (Gross) Job Reallocation Rate

$$
SUM_{jt} = POS_{jt} + NEG_{jt}
$$

**Decomposition:**

$$
SUM_{jt} =
(POS_{\text{Cont}} + NEG_{\text{Cont}}) +
(POS_{\text{Entry}} + NEG_{\text{Exit}})
$$

Upper bound (total reallocation volume):

$$
X_{jt}\,SUM_{jt} = X_{jt}(POS_{jt}+NEG_{jt})
$$

Lower bound (workers actually switching jobs):

$$
X_{jt}\,MAX_{jt} = X_{jt}\,\max(POS_{jt},NEG_{jt})
$$

---

## 10. Net Employment Growth Rate

$$
NET_{jt} = POS_{jt} - NEG_{jt}
$$

Positive → job expansion; Negative → contraction.

---

## 11. Excess Job Reallocation Rate

$$
EXC_{jt} = SUM_{jt} - |\;NET_{jt}\;|
$$

**Meaning:** Employment churn beyond what’s needed for net growth.

---

## 12. Persistence of Job Creation / Destruction

**Fraction of jobs created (or destroyed) in _t_ that persist in _t + k_:**

$$
\text{FPO}_{t1} =
\frac{\sum_{i:\text{NewJobs}_{it}>0}\text{NewJobs}_{it}}{POS_t},
\qquad
\text{FNE}_{t1} =
\frac{\sum_{i:\text{NewJobs}_{it}<0}|\text{NewJobs}_{it}|}{NEG_t}
$$

where \(\text{NewJobs}_{it} = \text{employment}_{it} - \text{employment}_{i,t-1}\).

---

## 13. Decomposition of Excess Job Reallocation

### Between-sector component

$$
\sum_{j=1}^{J}
\left|
\text{Net Emp Change}_j
\right|
-
\left|
\sum_{j=1}^{J}
\text{Net Emp Change}_j
\right|
$$

### Within-sector component

$$
\sum_{j=1}^{J}
\Big(
\text{Job Reallocation}_j
-
|\text{Net Emp Change}_j|
\Big)
$$

---

### 🧭 Interpretation Summary

| Indicator | Meaning | High Value → | Low Value → |
|------------|----------|---------------|--------------|
| **Turnover at the Top** | Leader changes | Dynamic market | Stable top firms |
| **Reshuffling** | Rank changes | Competitive | Persistent hierarchy |
| **Entry/Exit Rate** | Firm flows | Market fluidity | Barriers / stability |
| **Job Creation/Destruction** | Employment flows | Reallocation | Rigid structure |
| **Net Employment Growth** | Expansion vs shrinkage | Growing sector | Contraction |
| **Excess Reallocation** | Labor churn | Adjustment / Innovation | Static employment |
| **Persistence** | Longevity of jobs | Stable firms | Short-term churn |

---
