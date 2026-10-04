# Project: CardioView 3D — Multimodal AI Hackathon 2026, Track A

## Goal
Web app that predicts overall CAD and stenosis of LAD, LCX, RCA from clinical data (Z-Alizadeh Sani extension dataset, 303 patients) and shows the predictions on an interactive 3D heart.

## Hard rules
- NEVER use LAD, LCX, RCA, or Cath as input features (target leakage).
- Validation: repeated stratified 5-fold CV, tuning inside folds. Report mean ± std. No single train/test split as the headline.
- Calibrate probabilities (they drive artery colors).
- Never invent or hardcode metrics; all numbers come from running code.
- Visible medical disclaimer on every page: educational / decision support only, not a substitute for diagnostic imaging.
- 3D must run smoothly without a dedicated GPU.

## Stack
- Backend: Python, scikit-learn, XGBoost/LightGBM, SHAP, FastAPI
- Frontend: React + React Three Fiber (or plain Three.js)
- Repo layout: `/data`, `/notebooks`, `/backend`, `/frontend`, `/models`, `/docs`

## Judging weights
Predictive performance 30%, 3D visualization 25%, interpretability 20%, integration 15%, code quality 10%.
