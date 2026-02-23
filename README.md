# MSCS_634_Lab_4

## Purpose of the Lab
This lab explores regression modeling on the Diabetes dataset to understand how different approaches—Simple Linear Regression, Multiple Linear Regression, Polynomial Regression, Ridge, and Lasso—perform on the same prediction task. The goal is to compare model accuracy, generalization, and overfitting behavior.

## Key Insights from the Regression Analysis
- Using multiple features significantly improved performance over a single-feature model (`bmi` only).
- Higher polynomial degrees quickly led to overfitting: training error decreased while test error increased.
- Regularization improved generalization, with Lasso achieving the best test performance among tested models on this split.
- A balanced model complexity (rather than maximum complexity) produced better real-world predictive behavior.

## Challenges and Decisions During the Lab
- **Environment setup:** Missing packages (`scikit-learn`, `pandas`, `matplotlib`) caused initial execution errors and were installed in the notebook kernel.
- **Model design decisions:**
	- Chose `bmi` for simple linear regression as a clear single-feature baseline.
	- Used an 80/20 train-test split with `random_state=42` for reproducibility.
	- Evaluated all models with consistent metrics (MAE, MSE, RMSE, and $R^2$) for fair comparison.
- **Overfitting control:** Tested polynomial degrees and regularized models to explicitly assess bias-variance tradeoffs.