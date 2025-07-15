---
layout: default
title: Cox Regression – Cancer Survivability
---

[← Back to Projects](/Projects)

#  Cancer Survivability Using Cox Regression

## Summary

In this project, I applied the Cox Proportional Hazards model to explore survival patterns among cancer patients, using a clinical dataset initially containing over 12 million records. After filtering, the analysis focused on 10 million patients with survival indicators.

---

## Goals

- Predict time until event (death)
- Identify significant predictors of mortality
- Evaluate model assumptions and performance
- Visualize survival differences across groups

---

## Methodology

- **Model**: Cox Proportional Hazards using `lifelines` in Python
- **Variables**: Cancer stage, sex, survival time, alive/dead status
- **Metric**: Concordance index (~0.85)

The Cox model estimates how different variables (like stage or gender) impact the hazard of death over time without requiring the baseline hazard to be specified.

```math
h(t) = h₀(t) × exp(b₁X₁ + b₂X₂ + ... + bₚXₚ)

---

## Results

The Cox regression model performed well on the filtered SEER dataset, producing a **concordance index of approximately 85%**, meaning it correctly predicted survival order in 85% of cases. Coefficients from the model were interpretable:  

The dataset contained **6 million living and 4 million deceased** patients. Analysis revealed a sharp drop in survival during the early months post-diagnosis, consistent with clinical expectations in aggressive cancer types.

To visualize these patterns, a **Kaplan-Meier curve** was generated, showing survivability on the y-axis over time (x-axis: months since diagnosis). This revealed:
- A steep early decline in the number of surviving patients
- A more gradual drop-off as time progressed


These findings highlight the power of survival modeling for identifying high-risk groups and informing targeted interventions.
