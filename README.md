# Nifty50_weekly_prediction
This project implements a purely mathematical **Sequence-to-Sequence Multiple Linear Regression Model** built entirely from scratch in NumPy to predict the future intraday momentum of the NIFTY50 index.

## Overview
By framing the problem as **[Past 1875 Minutes] $\rightarrow$ [Future 1875 Minutes]**, the model learns a massive web of linear relationships (over 3.5 million distinct parameters). The model trains using basic Calculus (Gradient Descent) and effectively handles volatile market prices via strict Z-Score Standardization (ensuring no data leakage between train/test splits).

## Model Performance
Tested on a chronologically hidden 20% slice of the complete dataset:
- **$R^2$ Score**: 0.9276
- **Pearson Correlation**: 0.9762
- **Mean Absolute Error (MAE)**: 368.10

**Conclusion**: The custom sequence-to-sequence linear model successfully captures the core underlying momentum of the NIFTY index. The high accuracy on unseen test data proves that historical linear patterns are strong indicators of future intraday price movements.

## Project Structure
- `ml.ipynb` / `Nifty50_weekly_prediction.ipynb`: The core Jupyter Notebooks containing the data preprocessing, mathematics, and gradient descent implementation from scratch.
- `NIFTY_INTRADAY_2026.csv`: The complete NIFTY intraday historical dataset used for training and testing.
- `model.py`: Scratchpad/helper scripts for the model.

## How to Run
1. Clone this repository.
2. Ensure you have Python installed with the following dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```
3. Open and run the Jupyter Notebooks. The data loading cell points to the local CSV file in the repository.
