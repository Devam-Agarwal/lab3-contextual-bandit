# Lab 3: Contextual Bandit-Based News Recommendation System

**Student:** Devam Agarwal | **Roll Number:** U20230138  

---

## Lab Report

This project implements a contextual multi-armed bandit (CMAB) framework for personalized news recommendation.  
First, a classification model is trained to predict the user category (**user_1, user_2, user_3**) from contextual features. The predicted context is then used to choose among **12 total arms** (3 contexts × 4 categories per context) using bandit algorithms.

Models were trained using an **80/20 stratified train–validation split**. Since the feature matrix contained missing values, **median imputation** was applied (and scaling where required). The best classifier (Random Forest) was then used in a **10,000-step** bandit simulation to compare exploration strategies.

Three bandit methods were evaluated: **Epsilon-Greedy**, **SoftMax**, and **UCB**. Overall, **UCB** achieved the highest average reward, showing strong performance due to principled uncertainty-based exploration.

---

## Key Results

- **Classification Accuracy (Validation):** **0.9050** (Random Forest)
- **Simulation Horizon:** **T = 10,000** steps per algorithm
- **Best Algorithm:** **UCB (c = 1.0)** with **Avg Reward = 5.9469**
- **Average Rewards (best settings):**
  - **Epsilon-Greedy (ε = 0.05):** 5.6642  
  - **SoftMax (τ = 1.0):** 5.7649  
  - **UCB (c = 1.0):** 5.9469  

---
