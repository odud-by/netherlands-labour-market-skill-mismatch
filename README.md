# Skill Mismatch & Labour Force Participation — Empirical Analysis

> **[View Full Thesis](./Full_BSc_Thesis.pdf)**
> **[View R Markdown code](./Code.Rmd)**
> Panel data study | Netherlands (LISS, 2019–2022) | N = 5,277 observations

---

## What This Project Does

Uses longitudinal survey data from the Netherlands to quantify how being over-qualified, under-qualified, over-skilled, or under-skilled affects how much people work and how much they earn — with econometric controls for gender, age, education level, and sector.

---

## The Core Question

When a worker's skills or education don't match their job, does that show up in their pay and hours — and by how much?

---

## Methodology (Applied Summary)

| Choice | Rationale |
|---|---|
| **Panel data (4 years)** | Tracks the same individuals over time — more reliable than one-shot surveys |
| **Random Effects model** | Controls for unobserved individual traits (motivation, ability) without discarding time-invariant variables |
| **Dual dependent variables** | Hours worked *and* log wages — both used as proxies for labour force participation |
| **Self-reported mismatch** | Workers classified based on their own assessment of fit (microeconomic approach) |

Fixed Effects were tested but produced insignificant results — likely due to the short time window and unbalanced panel structure. Random Effects is the preferred specification.

---

## Key Findings

### On Earnings
- **Over-educated workers earn 6.6% less** than well-matched peers — closely replicating a benchmark finding from the literature (Sicherman, 1991: 7%)
- **Over-skilled workers earn 5.8% less** than skill-matched peers
- Under-educated and under-skilled wage differences were not statistically significant

### On Hours Worked
- **Over-educated workers work ~1hr 22min fewer hours per week**
- **Under-educated workers work ~1hr 51min more per week**
- Skill mismatch effects on hours were directionally consistent but not statistically significant

### Cross-cutting Signals
- **Gender wage gap is large and robust**: women earn ~30.9% less and work ~4.3 fewer hours per week, holding all else equal
- **Earnings strongly predict hours**: each unit increase in log wages corresponds to ~3.8 additional hours worked — higher pay motivates greater labour force participation

---

## What the Results Mean in Practice

**For over-educated/over-skilled workers:** Being overqualified isn't a career advantage — it's associated with lower pay and reduced engagement. Organisations that underpace workers on challenge and responsibility likely incur hidden productivity costs.

**For under-educated workers:** These workers compensate by putting in more hours. They are active, engaged participants — not a drag on productivity.

**For policymakers:** The gender gap is persistent even after controlling for sector, education level, and hours. Wage equity interventions need to go beyond sector-level solutions.

**For employers:** Mismatch — in either direction — signals suboptimal job design. Better role-to-person matching has a measurable wage and engagement dividend.

---

## Data & Scope

- **Source:** LISS Panel (Longitudinal Internet Studies for Social Sciences), managed by CentERdata / Tilburg University
- **Period:** 2019–2022
- **Final sample:** 5,277 observations, 2,786 unique respondents
- **Exclusions:** Students, retirees (65+), multi-job holders, unemployed
- **Geography:** Netherlands (assumed representative of Dutch working population)

---

## Limitations

- Short panel (4 years) limits the power of within-person estimation
- Self-reported mismatch only — no objective skill assessment data available
- Unbalanced panel introduces potential non-random attrition bias
- Omitted variables (job tenure, firm size, occupational detail) may affect precision

---

## Technical Stack

```
Language:     R
Models:       Pooled OLS · Fixed Effects · Random Effects (GLS)
Data format:  Unbalanced longitudinal panel
Key packages: plm, stargazer, ggplot2
```

---

*BSc Econometrics — University of Amsterdam | Department of Business and Economics*
