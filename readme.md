# Thermophysical Property: Melting Point

This project is for the [**Thermophysical Property: Melting Point** Kaggle Competition](https://www.kaggle.com/competitions/melting-point), which challenges participants to build Machine Learning models to predict the **melting point ($T_m$)** of organic compounds.

The goal is to develop models that effectively capture the complex, non-linear relationships between molecular structure and melting behavior using provided molecular descriptors.

---

## 🎯 Competition Goal and Metric

* **Goal**: Predict the melting point ($T_m$) in **Kelvin ($\text{K}$)** for organic compounds.
* **Evaluation Metric**: **Mean Absolute Error (MAE)** on a held-out test set.

$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$$

Where $y_i$ is the actual melting point and $\hat{y}_i$ is the predicted melting point for the $i$-th compound.

---

## 📁 Project Structure

The repository is organized as follows:

    .
    ├── data/                       # Raw competition data
    ├── notebooks/                  # Jupyter notebooks for EDA, experimentation, and final model training
    ├── src/                        # Python scripts (data processing, model training, model predictions, ...)
    ├── models/                     # Saved trained model files
    ├── submissions/                # CSV files of predictions ready for submission to Kaggle
    ├── README.md                   # This file
    ├── environment.yml             # Environment setup (using conda)
    └── requirements.txt            # List of dependencies (for non conda users)

---

## 🛠️ Setup and Execution

0. **Pre-requisites**
    * Start by installing [Anaconda](https://www.anaconda.com/download) (or [miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main)) and [git](https://git-scm.com/downloads).

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/MrIsCM/Thermophysical-Property-Comp.git
    cd Thermophysical-Property-Comp
    ```

2.  **Virtual Environment Setup**:
    * Create the virtual environment and install all dependencies:
        ```bash
        conda env create -f environment.yml
        conda activate kaggle-competitions
        python -m ipykernel install --user --name=python3
        ```

3.  **Data Download**:
    * Download the competition data files from the [Kaggle data page](https://www.kaggle.com/competitions/melting-point/data).
    * Place them inside the **`data/`** directory.

4.  **Run Experiments**:
    * Start with the notebooks in **`notebooks/`** for initial analysis and experimentation.
    * Final, clean model pipelines should be moved into `.py` files in the **`src/`** directory.

---

## 📈 Submissions Tracker

| Date | Notebook/Script | Model | MAE (Public LB) | Submission File | Notes |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 30/09/2025 | `notebooks\03-modeling.ipynb` | RF Regression | 33.950 | `submissions\base_rand_forest.csv` | Baseline. No hyperparameter tuning |
| 30/09/2025 | `notebooks\03-modeling.ipynb` | XGBoost Regression | 34.255 | `submissions\base_xgboost.csv` | Baseline. No hyperparameter tuning |
| 30/09/2025 | `notebooks\03-modeling.ipynb` | Linear Regression | 35.050 | `submissions\base_lin_reg.csv` | Baseline. No hyperparameter tuning |