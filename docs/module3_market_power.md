---
title: "Modules 3 & 4 – Performance and Market Power Indicators"
layout: default
---

# 5.3 Module 3 – Performance Indicators

## 1) Productivity (TFP)
**Definition.** Total Factor Productivity (TFP) is covered in detail in the next section.  
(Include your chosen TFP methodology here—e.g., OP/LP/Wooldridge.)

---

## 2) Value Added per Worker
**Definition.** Labor productivity at the firm level.

$$
\text{Value Added per Worker}_{ijt}
=
\frac{\text{Value Added}_{ijt}}{\text{Employment}_{ijt}}
$$

---

## 3) Firm Profit
**Definition.** Financial gains after costs.

$$
\text{Firm Profit}_{ijt} = \text{Total Revenue}_{ijt} - \text{Total Costs}_{ijt}
$$

---

## 4) Profit Rate
**Definition.** Profit as a share of revenue.

$$
\text{Profit Rate}_{ijt}
=
\frac{\text{Firm Profit}_{ijt}}{\text{Total Revenue}_{ijt}}
$$

---

# 5.4 Module 4 – Market Power Indicators

There are two prominent approaches to markups:

- **Demand approach:** estimate demand elasticities (e.g., BLP) and recover marginal costs from FOCs (Berry et al., 1995; 2004).
- **Production approach:** use inputs/outputs plus cost-minimization FOCs to infer marginal cost and markups (De Loecker & coauthors).

Both require assumptions (competition model on demand side; flexible variable input and production function on production side) and instruments/control functions for endogeneity.

---

## 5.4.1 Product Markups à la De Loecker et al. (2012, 2020)

**Markup** of firm \(i\) at time \(t\): price over marginal cost.

$$
\mu_{it} = \frac{P_{it}}{\lambda_{it}}
$$

\(\lambda_{it}\) is marginal cost.

---

## 5.4.2 Markup Estimation via the Accounting / Production Approach

**Technology (single variable input for exposition):**

$$
Q_{it} = Q_{it}(X_{it}, K_{it}, \omega_{it})
$$

Cost-minimization FOC (w.r.t. \(X\)), combined with \(\mu_{it} = \frac{P_{it}}{\lambda_{it}}\), yields the classic markup formula:

$$
\mu_{it}
=
\frac{\beta^X_{it}}{\alpha^X_{it}}
\quad\text{with}\quad
\beta^X_{it} \equiv
\frac{\partial Q_{it}}{\partial X_{it}}
\cdot
\frac{X_{it}}{Q_{it}},
\qquad
\alpha^X_{it} \equiv \frac{P^X_{it} X_{it}}{P_{it} Q_{it}}
$$

- \(\beta^X_{it}\): output elasticity of the variable input.  
- \(\alpha^X_{it}\): revenue share of that input.

**Examples of \(\alpha\):**
- If \(X=L\) (labor), \(P^X=W\):  
  \(\displaystyle \alpha^L_{it} = \frac{W_{it} L_{it}}{P_{it} Q_{it}}\)
- If using **COGS** as the variable input proxy:  
  \(\displaystyle \alpha^V_{it} = \frac{\text{COGS}_{it}}{\text{Total Revenue}_{it}}\)

**Note:** \(\beta\) must be estimated (proxy methods or cost-share approaches).

---

## 5.4.3 Factor Elasticities via Cost Shares

Assume Cobb–Douglas with two variable inputs (labor \(L\), materials \(M\)) and capital \(K\):

$$
Q_{it} = K_{it}^{\beta_k} L_{it}^{\beta_l} M_{it}^{\beta_m} \exp(\omega_{it})
$$

Using the factor demand system under \(\lambda_{it} = \frac{P_{it}}{\mu_{it}}\) and defining returns to scale \(RTS_{it}=\beta_k+\beta_l+\beta_m\), we get:

$$
\beta_l
=
\frac{W_{it} L_{it}}{RTS \cdot \left( r^K_{it} K_{it} + W_{it} L_{it} + P^M_{it} M_{it} \right)}
$$

**Operationalization (common in practice):**
- Use **industry-level** elasticities (time-averaged) to mitigate adjustment-cost issues.
- Often assume \(RTS=1\) (CRS) as a benchmark; do robustness with \(RTS<1\).

---

## 5.4.4 Factor Elasticities via Proxy Methods (OP/LP/Wooldridge)

Log output:

$$
y_{it} = \beta_0 + \beta_k k_{it} + \beta_l l_{it} + \beta_m m_{it} + \omega_{it} + \varepsilon_{it}
$$

Problem: inputs correlate with \(\omega_{it}\) (productivity).  
**Solution:** treat \(m_{it}\) as flexible; invert its demand to form a control function:
\(\omega_{it}=m^{-1}(k_{it},l_{it},m_{it})\).  
Then estimate in two stages (control-function approach), assuming Markov process for \(\omega_{it}\), and use moment conditions to identify \((\beta_k,\beta_l,\beta_m)\).

*(Include your chosen variant—OP, LP, or Wooldridge GMM—here.)*

---

## 5.4.5 Markups and Labor **Markdowns** à la Yeh, Macaluso & Hershbein (AER, 2022)

Let revenues be \(R_{it}=P_{it} Q_{it}\), production \(Q_{it}=Q_{it}(K,L,M;\omega_{it})\).  
Assume **one fully flexible input** \(j\) (no adjustment costs, competitive input market, static choice).

- If the flexible input is **materials**:
  
  $$
  \mu_{it} = \frac{\theta^m_{it}}{\alpha^m_{it}},
  \quad
  \theta^m_{it} \equiv \frac{\partial Q_{it}}{\partial M_{it}} \cdot \frac{M_{it}}{Q_{it}},
  \quad
  \alpha^m_{it} \equiv \frac{P^M_{it} M_{it}}{P_{it} Q_{it}}
  $$

- If labor markets are **non-competitive** (monopsony), define the **markdown** \(\nu_{it}\) as MRPL / wage. With output market power (markup \(\mu_{it}\)), one obtains:

  $$
  \nu_{it}
  =
  \frac{1}{\mu_{it}} \cdot \frac{\theta^\ell_{it}}{\alpha^\ell_{it}},
  \quad
  \theta^\ell_{it} \equiv \frac{\partial Q_{it}}{\partial L_{it}} \cdot \frac{L_{it}}{Q_{it}},
  \quad
  \alpha^\ell_{it} \equiv \frac{W_{it} L_{it}}{P_{it} Q_{it}}
  $$

**Interpretation:**  
- \(\mu>1\): **product** market power (price over marginal cost).  
- \(\nu>1\): **labor** market power (MRPL exceeds wage → markdown on labor).

---

## Practical Notes

- Choose **consistent sectors** and **time spans** for comparability.  
- For markups: report **distributions** (median, p10–p90), not just means.  
- Robustness: try **cost-share** vs **proxy** elasticities; CRS vs DRS; alternative flexible inputs.  
- Document **measurement choices**: COGS composition, wage bill definition, capital user costs, etc.

---
