# ML-Lasso-CV

<div align="justify"> 
  
Main objective is to identify the most influential features driving house prices & developing a predictive model in estimating house prices in the Boston area

Let’s first understand these methodologies

**Lasso regression** - is a linear regression model that includes a regularization term, which is a penalty for large regression coefficients. This penalty term helps to prevent overfitting and improves model generalization (how well the model predicts the unseen data)

**Cross-validation** - is used to assess the performance of a model. It's done by dividing the dataset into multiple folds and training the model on different combinations of these folds. The model is then tested on the fold that it was not trained on, and this process is repeated for each fold. The average performance of the model on all the folds is then calculated to give a more accurate estimate of how the model will perform on new unseen data.

**LASSO CV** - is used to find the optimal value of the regularization parameter lambda(λ). The basic idea of Lasso cross-validation is to fit the Lasso regression model with different values of lambda and evaluate the model performance using a cross-validation approach.

**Steps :**

**Data Preprocessing :**
Missing Values : drop , impute with mean, impute with median
Categorical variables - use one-hot encoding to convert them to numerical columns

**EDA :**
Boxplot - Price distribution across various regions
southern metropolitan has the highest price; with Eastern metropolitan being the 2nd highest

Boxplot - Building Area distribution for various number of bedrooms
Building area is increasing with the number of bedrooms. However, 5 bedroom has more built area than a 6 bedroom in boston.

Correlation - Price vs X variables
Building Area is highly correlated with the price of the house

Stacked Bar Chart - price distribution based on type & no of bedrooms
3 bedroom & 4 bedroom houses are higher priced in villa house type than in townhouse type

**Model Development & Evaluation :**

1. Linear regression with forward selection feature selection
- R squared = 50%
- MSE = $ 361 Billion
- AIC = 8.9K

2. LASSO CV
- optimal alpha = 2154
- R squared = 48.9%
- MSE = $ 372 Billion
- AIC = 11.8K

**Conclusion :** All the performance evaluators are in favour of the linear regression model over the lasso.

**Contributions** Feel free to submit pull requests or start an issue if you find a bug or have any suggestions for improving this notebook.
</div>
