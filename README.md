# Intelligent Freight Network Optimization

### A Decision Intelligence System for Cost- and Delay-Optimized Routing Across 37 Logistics Hubs

[LinkedIn](https://www.linkedin.com/in/damo-madhukar) | [GitHub](https://github.com/damo97-dsi/Freight_Optimization)

---

## 🚀 Executive Snapshot

* 🚛 Optimizes freight routing across 37 logistics hubs using ML + optimization
* 📊 Predicts cost, delay risk, and fuel consumption for decision inputs
* ⚙️ MILP-based optimization balancing cost (70%) and delay (30%)
* 💰 Achieved ~13% reduction in composite logistics cost
* 📦 Maintained ≥95% service-level performance under constraints
---
## 📌 Outcome: 
### Replaces rule-based routing with optimization-driven decision logic, reducing cost while maintaining service constraints.

## 📊 Sample Output

Key analytical outputs from the system:

### Cost vs Distance Relationship

![Cost Distance Correlation](visuals/correlation_heat_map.png)

### Fuel Consumption vs Load

![Fuel vs Load](visuals/fuelvstons.png)

### Optimization Impact (Baseline vs Optimized)

![Optimization Results](visuals/optimisation.png)

This comparison highlights the reduction in total logistics cost after applying constraint-based optimization, demonstrating measurable efficiency gains over baseline routing.

---

## Overview

📌 **Focus: Moving from heuristic routing → optimization-driven decision-making**

This project builds a decision intelligence system that integrates machine learning and mixed-integer linear optimization to improve freight routing decisions.

Using 180K+ simulated shipments across 37 hubs, the system predicts operational metrics and generates routing strategies that minimize cost while controlling delay risk and maintaining service constraints.

---

## Business Problem

Freight routing is often driven by static rules or local heuristics that fail to capture system-wide tradeoffs.

This leads to:

* inefficient routing decisions
* higher transportation cost
* avoidable delays
* poor network utilization

---

## Objective

Design a routing decision system that:

* predicts key operational metrics
* evaluates cost vs delay tradeoffs
* recommends optimized routing allocations under constraints

---

## Decision Pipeline

### 1. Data Intelligence

* analyzed shipment behavior across routes and hubs
* identified cost-distance relationships (~0.77 correlation)

### 2. Predictive Layer

Built models to estimate optimization inputs:

* Cost Prediction → R² ≈ 0.78
* Delay Prediction → R² ≈ 0.31
* Fuel Consumption → R² ≈ 0.99

These outputs serve as inputs to the optimization model.

### 3. Optimization Engine

Developed a Mixed-Integer Linear Programming (MILP) model using Pyomo + CBC.

**Objective:**

* minimize **0.7 × cost + 0.3 × delay**

**Constraints:**

* service level ≥ 95%
* delay threshold ≤ 3 hours
* network feasibility conditions

### 4. Decision Output

Generated optimized routing allocations across the network, improving efficiency while maintaining operational constraints.

---

## Key Results

| Metric         | Baseline | Optimized | Improvement    |
| -------------- | -------- | --------- | -------------- |
| Composite Cost | 572,817  | 498,886   | ~13% reduction |

#### This result demonstrates the effectiveness of model-driven routing over static or rule-based allocation approaches.
---

## Business Impact

* Reduced logistics cost by ~13% while maintaining ≥95% service levels
* Replaced heuristic routing with constraint-based optimization
* Demonstrated measurable efficiency gains in network-level decision-making
* Demonstrated superiority of optimization over rule-based routing
* Provided a scalable framework for network-level decision-making

---

## Tradeoff Design

The optimization balances efficiency and service reliability:

* **Cost (70%)** prioritized for operational efficiency
* **Delay (30%)** included to maintain service quality

This reflects real-world logistics decision tradeoffs.

---

## Modeling Notes

Delay prediction showed lower explanatory power (**R² ≈ 0.31**), indicating higher variability.

Instead of relying solely on prediction, constraints were used to control delay risk, making the system more robust.

---

## Tools & Technologies

Python · pandas · scikit-learn · XGBoost · Pyomo · CBC Solver · matplotlib

---

## Project Structure

```text
Freight_Optimization/
│
├── data/
├── notebooks/
├── visuals/
├── Intelligent_Freight_Network_Optimization.ipynb
├── requirements.txt
└── LICENSE
```

---

## Why This Project Matters

This project demonstrates how predictive analytics and optimization can move beyond analysis to drive real operational decisions.

It reflects how logistics systems transition from heuristic rules to model-driven, constraint-based decision frameworks.

Relevant for:
- Business Intelligence  
- Operations Analytics  
- Supply Chain Analytics  
- Decision Science  

---

## How to Run

```bash
git clone <repo-link>
cd Freight_Optimization
pip install -r requirements.txt
jupyter notebook
```

---

## Author

**Damodar Naraparaju**
Master’s in Business Analytics – Saint Peter’s University
