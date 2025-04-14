# ⚽ Ligue 1 Club Performance Analysis (2014–2024)

This project provides an exploratory data analysis (EDA) of club-level performance in Ligue 1 over ten seasons (2014–2024).  
The dataset aggregates season-level statistics per team and focuses on identifying the statistical drivers of success, consistency, and over/underperformance.

---

## 📁 Dataset Overview

The dataset includes:
- Seasonal statistics for each team (`Pts`, `GF`, `GA`, `Poss`, `CS%`, `PK`, etc.)
- Match-normalized metrics (e.g., `Pts_per_MP`) for comparability across seasons
- Final league rankings and match outcomes (wins, draws, losses)
- Coverage of the 2015–16 to 2023–24 seasons

---

## 🔎 1. Comparative Analysis: Long-term Clubs vs. Promoted/Relegated Teams

We compare the average performance of clubs that remained in Ligue 1 throughout the period vs. those that were promoted or relegated.  
Established clubs exhibit higher averages in points, possession, and defensive stats — revealing structural consistency.

---

## 📈 2. Evolution of Ligue 1 Performance Over Time

We track:
- Season-by-season evolution of goals, points, and possession
- Club-level trajectories for PSG, Lyon, and Monaco
- Stability and volatility of league rankings

---

## 📊 3. Variability of Team Rankings

Using numerical transformation of final rankings (`LgRank`), we compute:
- Average rank per team
- Rank standard deviation (stability)
Low mean + low variance → dominant and consistent teams.

---

## ⚔️ 4. Statistical Comparison of Clubs

- Average stats over the full period (e.g., possession, clean sheets)
- Radar charts to compare multi-dimensional team profiles

All stats were normalized to allow fair comparison.

---

## 🔁 5. Correlation Analysis

We explore relationships such as:
- Possession vs. Points
- Goals scored vs. Points
- Clean Sheets vs. Final Rank

A heatmap reveals the strongest performance correlations.

---

## 🧠 6. Success Factors and Top 3 Prediction

Classification models tested:
- Logistic Regression
- Decision Tree
- Random Forest

Main predictive features: `GF_per_MP`, `CS%`, and `Poss`.

---

## 📈 7. Modeled Ranking & Surprises

We generate Top 3 probability scores per club-season.  
This helps identify:
- Overperformers (e.g., Monaco 2016–17, Lille 2020–21)
- Underperformers by model expectation (e.g., Rennes 2021-22, Marseille 2017-18)

---

## 🧪 8. Offensive and Defensive Efficiency

We construct normalized metrics:
- Offensive Efficiency = (GF − PK) / Possession
- Defensive Efficiency = CS% / GA_per_MP

Combined to create a total performance score.

---

## 🎯 9. Penalty Analysis

We examine:
- Penalty frequency and conversion rate
- Share of total goals from penalties (`PK / GF`)
Some teams rely heavily on penalties to score.

---

## ✅ Conclusion & Future Work

This project revealed key performance drivers in Ligue 1 and built a statistical basis for modeling future outcomes.

Possible next steps:
- Match-level analysis
- Full-season simulation (e.g., Monaco 2019–20)
- Dashboard or API for interactive insights

---

## 📘 Variable Glossary

| Variable   | Description |
|------------|-------------|
| `Rk`       | Row index (changes with sorting) |
| `Season`   | Football season |
| `Comp`     | Competition name |
| `MP`       | Matches Played |
| `W/D/L`    | Wins / Draws / Losses |
| `Pts`      | Points (3 per win, 1 per draw) |
| `Pts/MP`   | Points per Match |
| `LgRank`   | Final League Rank |
| `GF`       | Goals For |
| `GA`       | Goals Against |
| `GD`       | Goal Difference |
| `Poss`     | Possession (%) |
| `CS`       | Clean Sheets |
| `CS%`      | Clean Sheet Percentage |
| `G-PK`     | Non-Penalty Goals |
| `PK`       | Penalty Kicks Made |
| `PKatt`    | Penalty Kicks Attempted |
| `PKm`      | Penalty Kicks Missed |
| `Subs`     | Games played as substitute |
| `Min`      | Total minutes played |

