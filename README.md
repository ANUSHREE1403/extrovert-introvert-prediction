# Extrovert vs Introvert Personality Prediction

This repository contains my submission for the **Kaggle Playground Series - S5E7** competition.  
The task was to classify people as **Introvert** or **Extrovert** based on various features.

---

## File Included

- `submission_fixed.csv`  
  Contains final predictions  
  Follows required Kaggle format:  
  `id,Personality` → where `Personality` is either `Introvert` or `Extrovert`

---

## Fix Implemented

The original predictions were numeric (`0` for Extrovert and `1` for Introvert),  
but Kaggle required labels as **strings**.

So I mapped the values:
```python
df["Personality"] = df["Personality"].map({0: "Extrovert", 1: "Introvert"})

