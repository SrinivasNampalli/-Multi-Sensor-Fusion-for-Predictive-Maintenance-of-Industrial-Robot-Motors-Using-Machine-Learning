# Motor Predictive Maintenance Analysis

This project implements a multi-sensor fusion approach for predictive maintenance of industrial robot motors using machine learning. It analyzes sensor data (temperature, voltage, position) to detect anomalies and predict potential failures.

## Project Structure

```
├── data/               # Data directory
│   └── raw/            # Raw sensor data (CSV files per session/motor)
├── docs/               # Documentation
├── figures/            # Generated figures for reports/papers
├── models/             # Directory for saving trained models
├── plots/              # Generated plots and dashboards
├── scripts/            # Executable scripts for analysis and training
│   ├── main_analysis.py          # Main complete analysis pipeline
│   ├── train_and_save_models.py  # Train ML models and save them
│   ├── generate_ieee_figures.py  # Generate publication-quality figures
│   ├── model_predictor.py        # Class for making predictions
│   ├── use_trained_models.py     # Example usage of trained models
│   └── test_models.py            # Unit tests for models
├── src/                # Source code modules
│   ├── data_loader.py            # Data loading and processing
│   ├── eda_visualizer.py         # Exploratory Data Analysis & Visualization
│   └── ml_models.py              # Machine Learning model definitions
└── requirements.txt    # Python dependencies
```

## Setup

1.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### 1. Run Complete Analysis
To run the full analysis pipeline, including data loading, EDA, anomaly detection, and report generation:

```bash
python scripts/main_analysis.py
```
This will generate:
-   A research report: `Motor_Predictive_Maintenance_Report.md`
-   Visualizations in the `plots/` directory.

### 2. Train and Save Models
To train the Random Forest and XGBoost models and save them for later use:

```bash
python scripts/train_and_save_models.py
```
Models will be saved in `saved_models/`.

### 3. Generate Publication Figures
To generate high-quality, IEEE-compliant figures for the research paper:

```bash
python scripts/generate_ieee_figures.py
```
Figures will be saved in `plots/` with "ieee_" prefix.

### 4. Make Predictions
To use the trained models for making predictions on new data, see `scripts/use_trained_models.py` for examples.

## Key Features
-   **Data Loading**: Handles multiple test sessions and motor data files.
-   **Anomaly Detection**: Uses IQR and Z-score methods to identify outliers.
-   **Machine Learning**: Implements Random Forest and XGBoost classifiers for failure prediction.
-   **Visualization**: Comprehensive dashboards for data distribution, correlations, and model performance.
