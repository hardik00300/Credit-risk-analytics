# Credit Risk Analytics Framework

This project builds a Python-based credit risk analytics framework to understand how a bank monitors and manages portfolio credit risk **before defaults materialize**.

The analysis is performed on a **hypothetical bank loan portfolio**, designed to closely mirror real-world credit risk behavior.

---

## Key Objectives

- Track how portfolio credit risk evolves over time
- Measure Expected Loss using industry-standard risk metrics
- Identify early warning signals of portfolio deterioration
- Stress test the portfolio under adverse scenarios

---

## Core Risk Concepts Used

- **Probability of Default (PD)**
- **Loss Given Default (LGD)**
- **Exposure at Default (EAD)**
- **Expected Loss (EL = PD × LGD × EAD)**
- **Credit Rating Migration**
- **Cumulative Default Risk**
- **Stress Testing & Scenario Analysis**

---

## What This Model Does

### 1. Portfolio Risk Measurement
- Calculates one-year and cumulative PD across credit ratings
- Computes rating-wise and portfolio-level Expected Loss
- Tracks EL as a percentage of total exposure

### 2. Rating Migration & Stability
- Analyzes transition matrices year-over-year
- Identifies which rating categories exhibit the highest stability
- Highlights long-term deterioration patterns

### 3. Stress Testing
Two stress scenarios are implemented:
- **LGD Shock**: Simulates downturn conditions by inflating LGD values
- **Rating Slip Scenario**: Forces downgrades across rating buckets to test tail risk

### 4. Risk Shift Monitoring
A simple risk dashboard is constructed using:
- Portfolio PD trends
- Expected Loss as % of EAD
- Exposure concentration in high-risk ratings

This helps detect **gradual risk build-up**, not just sudden defaults.

---

## Data

- The dataset represents a **hypothetical bank portfolio**
- Includes borrower-level exposures, ratings, LGD, and EAD factors
- Structured to resemble real internal bank risk data

---

## Tech Stack

- Python
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

---

## Why This Matters

Credit risk rarely explodes overnight.  
It usually shows up first as:
- Rising PD volatility
- Increasing exposure to weaker ratings
- Widening gaps between stressed and base-case expected loss

This framework demonstrates **how banks actually monitor those signals**.

---

