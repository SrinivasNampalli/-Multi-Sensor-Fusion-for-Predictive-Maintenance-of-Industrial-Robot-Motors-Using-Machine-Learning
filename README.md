# Motor Predictive Maintenance Analysis

Predictive maintenance for industrial robot motors using machine learning. This combines data from different sensors (temperature, voltage, position) to Spot anomalies and catch potential failures early.

## Project Structure

```
├── data/               # Data directory
├── docs/               # Documentation
├── figures/            # Figures for the paper
├── models/             # Saved models
├── plots/              # Plots and dashboards
├── scripts/            # Analysis and training scripts
├── src/                # Source code
└── requirements.txt    # Dependencies
```

## Setup

1.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### 1. Run Analysis
Runs the data loading, analysis, and report generation.

```bash
python scripts/main_analysis.py
```
Outputs:
-   Report: `Motor_Predictive_Maintenance_Report.md`
-   Visualizations in `plots/`

### 2. Train Models
Train the models (Random Forest, XGBoost) and save them.

```bash
python scripts/train_and_save_models.py
```
Models go in `saved_models/`.

### 3. Generate Diagrams
Create the figures used in the paper.

```bash
python scripts/generate_ieee_figures.py
```
Figures go in `plots/`.

### 4. Make Predictions
See `scripts/use_trained_models.py` for how to run predictions on new data.

## Features
-   **Data Loading**: Handles the raw motor session files.
-   **Anomaly Detection**: Spots outliers using standard statistical methods.
-   **Machine Learning**: Uses Random Forest and XGBoost.
-   **Visualization**: diverse plots for data and model performance.
