# ⚽ FIFA World Cup 2026 Predictions Using Machine Learning

A complete end-to-end machine learning project that predicts the FIFA World Cup 2026 tournament using historical World Cup results, FIFA rankings, ELO ratings, statistical modeling, and Monte Carlo simulation.


https://github.com/pavanharshavardhan/FIFA-WC-2026-ML-Prediction

The project combines data engineering, feature engineering, predictive modeling, probabilistic simulation, and sports analytics to estimate:

* Tournament winner probabilities
* Knockout-stage qualification odds
* Group-stage standings
* Dark horse teams
* Golden Boot (top scorer) candidates
* Defensive rankings
* Group difficulty analysis
* Tournament-wide statistical insights

---
<img width="578" height="353" alt="Fifa db1" src="https://github.com/user-attachments/assets/f853c4ab-d6b4-46fa-97e5-3bece2ff866c" />
<img width="580" height="355" alt="Fifa db2" src="https://github.com/user-attachments/assets/bd79a0e1-6258-43d9-b116-4b73c9e72558" />

## Key Results

| Prediction | Result |
|------------|---------|
| Most Likely Winner | France (10.6%) |
| Runner-Up Favorite | Brazil (9.5%) |
| Dark Horse | Colombia |
| Golden Boot Favorite | Kylian Mbappé |
| Hardest Group | Group K |
| Highest Scoring Group | Group B |
| Simulations | 50,000 |
| Final Model | XGBoost |


## Project Overview

Predicting an international football tournament is inherently uncertain due to limited matches, evolving team strength, and knockout-stage variance.

To address this challenge, this project builds a data-driven simulation framework using:

1. Historical FIFA World Cup matches (1930–2022)
2. FIFA World Rankings (2026)
3. Team ELO ratings derived from historical World Cup performance
4. Head-to-head tournament records
5. Team scoring and defensive statistics
6. Monte Carlo tournament simulations

The result is a probabilistic forecast of the entire FIFA World Cup 2026 tournament.

---

## Dataset Sources

### FIFA Rankings

* FIFA Rankings (October 2022)
* FIFA Rankings (June 2026)

Used for:

* Team strength estimation
* Ranking-based features
* FIFA points integration

### Historical World Cup Matches

* World Cup matches from 1930–2022

Used for:

* ELO rating computation
* Model training
* Historical team performance metrics
* Head-to-head statistics

### FIFA World Cup 2026 Schedule

* Official tournament fixture structure

Used for:

* Group-stage simulation
* Knockout bracket generation

### World Cup Historical Summary

Used for:

* Champion statistics
* Top scorer analysis
* Historical trends

---

## Methodology

### 1. ELO Rating System

An ELO model is built from scratch using every FIFA World Cup match since 1930.

Features:

* Dynamic rating updates
* Higher weighting for knockout matches
* Historical performance tracking

The ELO system provides a long-term measure of tournament strength independent of FIFA rankings.

---

### 2. Feature Engineering

For every match, the model generates:

#### Team Strength Features

* FIFA ranking
* FIFA points
* ELO rating
* Composite strength index

#### Historical Performance Features

* World Cup appearances
* Goals scored
* Goals conceded
* Win rate
* Recent tournament form

#### Head-to-Head Features

* Wins
* Draws
* Losses
* Goal differential

#### Relative Match Features

* ELO difference
* FIFA ranking difference
* Strength differential

---

### 3. Match Outcome Prediction

The project trains multiple machine learning models to predict:

* Home Win
* Draw
* Away Win

Models evaluated:

* Logistic Regression
* Random Forest
* XGBoost

Probability calibration is applied to improve simulation realism.

The best-performing model is selected and used throughout tournament simulations.

---

### 4. Tournament Simulation

The trained model powers a Monte Carlo tournament simulator.

For each simulation:

1. Group-stage matches are played probabilistically.
2. Teams advance based on points and tiebreakers.
3. Knockout rounds are simulated.
4. Tournament winner is recorded.

Thousands of simulations are run to estimate probabilities.

---

## Key Outputs

### Tournament Winner Probabilities

Ranks every qualified team by championship likelihood.

### Knockout Advancement Odds

Probability of reaching:

* Round of 32
* Round of 16
* Quarterfinals
* Semifinals
* Final
* Champion

### Group Stage Predictions

Projected standings and qualification probabilities.

### Dark Horse Analysis

Identifies teams with strong advancement odds despite lower rankings.

### Golden Boot Forecast

Estimates likely top scorers based on:

* Team offensive strength
* Expected tournament progression
* Historical scoring trends

### Defensive Rankings

Expected goals conceded analysis.

### Group of Death Detection

Measures competitive balance and group difficulty.

---

## Visualizations

The notebook includes:

* Team strength rankings
* ELO history charts
* Feature importance analysis
* Knockout probability distributions
* Golden Boot probabilities
* Defensive rankings
* Tournament dashboard
* Group difficulty analysis

---

## Tech Stack

**Programming**

* Python

**Data Analysis**

* Pandas
* NumPy

**Machine Learning**

* Scikit-Learn
* XGBoost

**Visualization**

* Matplotlib
* Seaborn

**Simulation**

* Monte Carlo Methods

---

## Project Structure

```text
FIFA-WC2026-Predictions/
│
├── FIFA_WC2026_Predictions.ipynb
├── data/
│   ├── fifa_ranking_2022.csv
│   ├── fifa_ranking_2026.csv
│   ├── matches_1930_2022.csv
│   ├── schedule_2026.csv
│   └── world_cup.csv
│
├── images/
│   └── dashboard.png
│
└── README.md
```

---

## Future Improvements

* Incorporate player-level statistics
* Include club form and injury information
* Add expected goals (xG) metrics
* Bayesian rating updates
* Ensemble prediction framework
* Live tournament updating during World Cup 2026

---

## Results

This project demonstrates how historical football data, ranking systems, machine learning, and probabilistic simulation can be combined to generate realistic tournament forecasts.

Rather than predicting a single winner, the framework estimates a full probability distribution of tournament outcomes, providing deeper insight into team strength, uncertainty, and competitive dynamics.

---

## Author

**Pavan Harsha Vardhan Gandu**

Machine Learning Engineer | M.S. Computer Science

Interests:

* Machine Learning
* Sports Analytics
* Ranking Systems
* Predictive Modeling
* Large-Scale Data Systems
