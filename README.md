# PlateWise AI — Restaurant Food Waste Prediction & Planning System

A small, responsive, static project showcase for explaining the Three Agent project to an academic audience.

## What's included

- `index.html` — overview, pipeline, interactive agent explainer, model evidence and preparation-planner demo.
- `style.css` — responsive visual design.
- `script.js` — agent tabs and live preparation calculation.
- `Agent123.ipynb` — the original Google Colab notebook copied into this project.

## Run locally in VS Code

1. Extract this folder and open it in VS Code.
2. Install the **Live Server** extension (or use any static HTTP server).
3. Right-click `index.html` → **Open with Live Server**.

No Python environment or backend is required for this showcase page. The planner is a browser-side illustration of Agent 2's formula; it does not call the CatBoost model.

## Publish with GitHub Pages

1. Create a new GitHub repository, e.g. `restaurant-food-waste-ai`.
2. Upload the contents of this folder to the repository root (so `index.html` is at the root).
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.
6. Wait for deployment and open the Pages URL shown in Settings → Pages.

## Project facts shown on the page

- CatBoost validation metrics: MAE 80.42, RMSE 165.70, WAPE 32.42%.
- Training weeks: 1–116; validation weeks: 117–145.
- Preparation target: `ceil(predicted demand × (1 + safety buffer))`.
- Recommended preparation: `max(0, target quantity − usable stock)`.

## Important scope notes

- Integrated demonstration inventory is simulated; it is not a live stock feed.
- The public demand dataset contains order demand, not measured discarded-food quantities. Potential surplus is an estimate, not verified food waste.
- SHAP values describe model behaviour, not causation.
- GitHub Pages hosts static files only. This page is an explanatory showcase, not the live Streamlit/CatBoost application. The original notebook is included for academic reproducibility; do not upload large datasets or private credentials.
