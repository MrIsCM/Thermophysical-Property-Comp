# Melting Point Prediction Challenge

This project is for the **Thermophysical Property: Melting Point** Kaggle Competition, which challenges participants to build Machine Learning (ML) models to predict the **melting point ($T_m$)** of organic compounds.

The goal is to develop models that effectively capture the complex, non-linear relationships between molecular structure and melting behavior using provided molecular descriptors (group contribution features).

---

## 🎯 Competition Goal and Metric

* **Goal**: Predict the melting point ($T_m$) in **Kelvin ($\text{K}$)** for organic compounds.
* **Evaluation Metric**: **Mean Absolute Error (MAE)** on a held-out test set. **Lower MAE is better.**

$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$$

Where $y_i$ is the actual melting point and $\hat{y}_i$ is the predicted melting point for the $i$-th compound.

---

## 📁 Project Structure

The repository is organized as follows:

You got it. Here is the README file content in Markdown format, ready to be saved as README.md.
Markdown

# Melting Point Prediction Challenge

This project is for the **Thermophysical Property: Melting Point** Kaggle Competition, which challenges participants to build Machine Learning (ML) models to predict the **melting point ($T_m$)** of organic compounds.

The goal is to develop models that effectively capture the complex, non-linear relationships between molecular structure and melting behavior using provided molecular descriptors (group contribution features).

---

## 🎯 Competition Goal and Metric

* **Goal**: Predict the melting point ($T_m$) in **Kelvin ($\text{K}$)** for organic compounds.
* **Evaluation Metric**: **Mean Absolute Error (MAE)** on a held-out test set. **Lower MAE is better.**

$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$$

Where $y_i$ is the actual melting point and $\hat{y}_i$ is the predicted melting point for the $i$-th compound.

---

## 📁 Project Structure

The repository is organized as follows:

    .
    ├── data/                       # Raw competition data (train.csv, test.csv, etc.)
    ├── notebooks/                  # Jupyter notebooks for EDA, experimentation, and final model training
    ├── src/                        # Python scripts (e.g., data preprocessing, feature engineering, model definitions)
    ├── models/                     # Saved trained model files
    ├── submissions/                # CSV files of predictions ready for submission to Kaggle
    ├── README.md                   # This file
    ├── environment.yml             # Environment setup (prefered)
    └── requirements.txt            # List of dependencies (backup)


## 🛠️ Setup and Execution

1.  **Clone the Repository**:
    ```bash
    git clone repo_name
    cd repo_name
    ```

2.  **Install Dependencies**:
    * It's highly recommended to use a conda virtual environment.
    * Install all required packages:
        ```bash
        pip install -r requirements.txt
        ```

3.  **Data Download**:
    * Download the competition data files from the [Kaggle data page](https://www.kaggle.com/competitions/melting-point/data).
    * Place them inside the **`data/`** directory.

4.  **Run Experiments**:
    * Start with the notebooks in **`notebooks/`** for initial analysis and experimentation.
    * Final, clean model pipelines should be moved into the **`src/`** directory.

---

## 📈 Submissions Tracker

| Date | Notebook/Script | Model | MAE (Public LB) | Submission File | Notes |
| :---: | :---: | :---: | :---: | :---: | :---: |
| TBD | `notebooks/01_baseline_model.ipynb` | Ridge Regression | TBD | `submissions/baseline_v1.csv` | Initial submission using basic features. |
| TBD | `src/train_catboost.py` | CatBoost + Optuna | TBD | `submissions/catboost_optuna_v2.csv` | Optimized hyperparameters with cross-validation. |
| TBD | TBD | TBD | TBD | `submissions/TBD.csv` | Final selection for private leaderboard. |