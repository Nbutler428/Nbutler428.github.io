---
layout: default
title: Cox Regression – Cancer Survivability
---

[← Back to Projects](/projects)

# 📈 Cancer Survivability Using Cox Regression

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

The Cox model estimates how different variables (like stage or gender) impact the hazard of death over time:

\\[
h(t) = h_0(t) \times \exp(b_1 X_1 + b_2 X_2 + \ldots + b_p X_p)
\\]

---

## Results

The Cox regression model performed well on the filtered SEER dataset, producing a **concordance index of approximately 85%**. This means it correctly predicted survival order in 85% of cases.

The dataset contained **6 million living and 4 million deceased** patients. A **Kaplan-Meier curve** showed:

- A sharp early decline in survivability
- A more gradual decline later
- Clear survivability differences by sex and stage

[![Survivability Graph](/assets/img/stage-rate.png)](/assets/img/stage-rate.png)

These findings highlight the power of survival modeling for identifying high-risk groups and informing targeted interventions.
