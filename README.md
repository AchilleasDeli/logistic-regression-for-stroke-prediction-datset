Project Description
Stroke Prediction using Logistic Regression
This project focuses on building a Logistic Regression model to predict the likelihood of a stroke based on patient data. The dataset includes both numerical and categorical features, which are preprocessed appropriately before model training.

Key Steps in the Notebook:
1. Data Loading & Initial Exploration
Loaded the dataset from an Excel file.

Identified numerical and categorical features.

Explored the data structure and missing values.

2. Data Preprocessing
Created dummy variables for categorical features using pd.get_dummies() with drop_first=True to avoid the dummy variable trap.

Ensured all dummy variables are binary (0 or 1).

Scaled all features using MinMaxScaler() from sklearn:

Numerical features were scaled to the range [0,1].

Dummy (categorical) variables remained 0 or 1 because they were already in that range.

3. Multicollinearity Check
Used Variance Inflation Factor (VIF) to check for multicollinearity among features.

Confirmed that VIF values were within acceptable limits, indicating no strong multicollinearity.

4. Model Building
Built a Logistic Regression model using sklearn to classify whether a patient is likely to have a stroke.

The target variable is stroke.

5. Handling Imbalanced Data
The dataset was imbalanced (many more non-stroke cases).

Used undersampling techniques to balance the target variable and avoid bias in predictions.

6. Model Evaluation
Evaluated the model performance using:

Accuracy

Classification Report (Precision, Recall, F1-score)

Checked whether the model performs well after balancing the dataset.

Tools & Libraries Used:
Python

Pandas

Numpy

Scikit-learn

Seaborn & Matplotlib (for visualizations)

Statsmodels (for VIF calculation)

Project Goal:
To build an interpretable and clean Logistic Regression model that can help predict the probability of a stroke using healthcare-related features, while ensuring correct preprocessing of mixed-type data.

