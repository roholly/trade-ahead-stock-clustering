# Trade & Ahead: Stock Clustering for Portfolio Diversification

**Domain:** Finance · Portfolio Analytics  
**Tools:** Python, scikit-learn, SciPy, yellowbrick  

---

## The Problem

A well-diversified stock portfolio shouldn't move in lockstep. If everything you own reacts the same way to the same market conditions, you haven't actually diversified. But identifying which stocks behave differently from each other across hundreds of companies and dozens of financial metrics is not something you do by hand.

Trade&Ahead, a financial consultancy, provided data on 337 NYSE-listed companies spanning 11 economic sectors. The goal was to group them by shared financial behavior and translate those groups into investor profiles with practical meaning.

---

## The Approach

Two clustering methods were applied independently and their results compared.

The first, K-Means, partitions companies into a set number of groups by minimizing the distance between each company and its group center. Testing from 2 to 14 groups, five produced the best balance between statistical validity and practical usefulness. Two groups was technically optimal but analytically useless for portfolio construction.

The second, hierarchical clustering, builds groups by successively merging the most similar companies and works its way up. Several merging strategies were tested. The one with the highest statistical score packed 334 of 337 companies into a single group. The one that produced the most interpretable and balanced grouping was selected instead, even at a lower score. Five groups again.

Both methods landed on the same five investor archetypes independently.

---

## What the Data Found

**The Majority** (275 companies): Broadly diversified across sectors, relatively stable, moderate returns. The foundation of most long-term portfolios. Nearly every sector is represented.

**Value Stocks** (9 companies): Household names you'd recognize: JPMorgan, Wells Fargo, AT&T, Verizon, Ford, Coca-Cola, Pfizer, Exxon. Large, stable, inexpensive per share relative to earnings. Low risk, steady long-term growth.

**Cash-Rich Growth** (24 companies): Primarily Healthcare and Information Technology. High liquidity, strong earnings per share, and the biggest price appreciation over the analysis period. More expensive per share, but the financials back it up.

**Energy** (30 companies): Predominantly oil and gas. High price-to-earnings ratios, steepest price decline over the period, and the highest volatility of any group. Cyclical by nature and sensitive to short-term market forces. The price drop at the time of analysis presented a potential buying opportunity for investors with the right risk tolerance.

**Speculative Energy** (2 companies, K-Means only): Apache Corporation and Chesapeake Energy, isolated from the broader energy group by their extreme volatility, negative earnings, and rock-bottom share price. High risk, high speculation.

---

## Key Finding

No sector labels were used as inputs. The groupings emerged entirely from financial metrics. That they mapped so cleanly onto recognizable investor archetypes, and that both methods arrived at the same five profiles independently, suggests the underlying financial structure of these companies is genuinely distinct across groups, not just statistically convenient.

---

## What This Demonstrates

- Translating unsupervised clustering results into actionable business recommendations
- Selecting methods based on interpretability, not just statistical performance
- Financial domain fluency applied to a real portfolio construction problem
