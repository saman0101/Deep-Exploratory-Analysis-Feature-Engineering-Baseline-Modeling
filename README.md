# Deep-Exploratory Analysis Feature Engineering & Baseline Modeling
## Model Selection

Four regression models were evaluated: **Linear Regression**, **Ridge Regression**, **Decision Tree Regressor**, and **Random Forest Regressor**. Model performance was assessed using MAE, RMSE, R², and 5-fold cross-validation to measure both predictive accuracy and generalization.

Among the evaluated models, the **Random Forest Regressor** achieved the best overall performance. It produced the lowest mean cross-validation RMSE of **0.934**, outperforming the Decision Tree Regressor (**1.501**), Linear Regression (**7.852**), and Ridge Regression (**7.852**). The large performance gap indicates that the relationship between the input features and energy consumption is likely nonlinear, making tree-based ensemble methods more suitable than linear models.

The Decision Tree Regressor also performed well but was consistently less accurate than the Random Forest. This is expected because Random Forest combines predictions from multiple decision trees, reducing variance and improving stability. Linear Regression and Ridge Regression produced very similar results, suggesting that regularization had little effect on model performance and that a simple linear relationship was insufficient to model the data.

The cross-validation results for the Random Forest were consistent across all five folds, with RMSE values ranging from approximately **0.82** to **1.16**. This relatively small variation suggests that the model generalizes well to unseen data. Although tree-based models can overfit, the agreement between the cross-validation performance and the test-set evaluation did not indicate severe overfitting.

Based on these results, the **Random Forest Regressor** was selected as the final baseline model and will be carried forward for future experimentation and model improvement.
