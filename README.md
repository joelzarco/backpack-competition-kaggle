# Backpack Price Prediction - Kaggle Playground Series S5E2

This project tackles the machine learning regression problem from Kaggle's Playground Series S5E2, focused on predicting backpack prices.

**Competition Link:** [Kaggle Playground Series S5E2 Overview](https://www.kaggle.com/competitions/playground-series-s5e2/overview)

This competition provides an excellent platform to hone machine learning skills using a synthetically generated dataset of approximately 300,000 entries. Each entry describes various features of a backpack and its corresponding price. The goal is to accurately predict the price based on these features, minimizing the Root Mean Squared Error (rMSE).

## Project Structure

My approach was structured as follows:

1.  **Exploratory Data Analysis (EDA):**

    *   **Data Exploration:** Identification of missing values in each column and analysis of column distributions to detect potential class imbalances.
    *   **Data Processing:** Evaluation and application of appropriate techniques for handling missing values in each column.

2.  **Model Development and Experimentation:**

    *   **Strategy 1:** Ordinal Encoding (Size) + One-Hot Encoding (Other Categorical Features)
        *   Model: LightGBM, fine-tuned with Optuna (100 trials)
        *   Result: rMSE = 38.9085
    *   **Strategy 2:** Ordinal Encoding (Size) + Target Encoding (Brand, Material, Style, Color)
        *   Model: LightGBM, fine-tuned with Optuna (100 trials)
        *   Result: rMSE = 38.9081
    *   **Strategy 3:** Ordinal Encoding (Size) + Target Encoding (Brand, Material, Style, Color)
        *   Model: XGBoost, fine-tuned with Optuna
        *   Result: rMSE = 38.9062

## Results and Future Improvements

While each of the three strategies yielded results within 0.01% of the winning solution (38.8333), this difference is significant in competitive Kaggle scenarios.

Potential future improvements include:

*   **Feature Engineering:** Creating new features from existing ones to potentially improve model performance.
*   **Advanced Encoding Techniques:** Exploring more sophisticated encoding methods to better represent categorical variables.