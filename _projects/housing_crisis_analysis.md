---
title: "U.S. Housing Crisis Analysis Using FHFA Data"
date: 2025-07-01
tools: "Python, Pandas, Scikit-learn"
description: "Analyzed regional housing market trends and the impact of the 2008 crisis using FHFA House Price Index data to identify risk factors and inform policy."
layout: default
---

## Overview

The late 2000s housing crisis devastated the U.S. economy, triggering foreclosures and collapsing home values. This project leverages the Federal Housing Finance Agency (FHFA) House Price Index to understand the crisis's impact on regional markets and identify contributing factors. By analyzing historical patterns, we aim to empower policymakers and homebuyers with insights to mitigate future risks.

## Key Steps

- **Data Processing**: Cleaned and transformed FHFA's "All-Transactions Indexes" (1975-2023) by combining year/quarter columns into date fields and pivoting regional data for analysis
- **Exploratory Analysis**: Conducted comparative analysis of 10 U.S. regions to identify disparities in price trends and market synchronization
- **Predictive Modeling**: Built linear regression models to predict national housing trends from regional indices and assess correlation patterns
- **Visualization**: Created time-series visualizations to illustrate recession impacts and regional recovery patterns

## Results & Insights

- **Regional Disparities**: Pacific and Mountain regions showed highest price indices (peaking at 942.52 and 727.52 respectively), while North Central regions remained more affordable with slower growth
- **Market Interconnection**: Discovered near-perfect correlation (r > 0.95) between regional markets, indicating limited diversification opportunities and systemic risk
- **Crisis Impact Analysis**: The 2008 crisis caused sharp, prolonged declines across all regions, with recovery rates varying significantly (New England rebounded 40% faster than West North Central)
- **Predictive Power**: Regional indices explain 99.97% of national variance (R²: 0.9997), enabling accurate forecasting for policy planning

## Policy Implications

The analysis reveals that housing markets are deeply interconnected yet regionally heterogeneous. Key recommendations include strengthening mortgage regulations, monitoring high-growth regions for bubbles, and leveraging predictive modeling for proactive interventions to avert future crises.

---

View this project on the website: [U.S. Housing Crisis Analysis]({{ site.baseurl }}/projects/housing_crisis.html)

### Relevant Sources
- [FHFA Data Portal](https://www.fhfa.gov/DataTools/Downloads)
- [Subprime Mortgage Crisis (2008)](https://en.wikipedia.org/wiki/Subprime_mortgage_crisis)
- [1995 Housing Market Analysis](https://www.cutimes.com/2018/12/14/trouble-in-housing-looks-more-like-1994-than-2007)
