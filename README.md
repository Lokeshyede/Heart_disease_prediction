# Heart_disease_prediction
Developed a predictive model to detect heart disease based on health data using Python, Scikit-learn, and Pandas. Deployed the project on GitHub for version control and sharing, demonstrating data preprocessing, model training, and performance evaluation.
📓 Project Workflow
The notebook follows a standard machine learning pipeline:

Data Loading: The dataset heart.csv is loaded into a pandas DataFrame.

Exploratory Data Analysis (EDA):

Initial Inspection: The dataset contains 918 rows and 12 columns.

Data Types: Features include numerical (Age, RestingBP, Cholesterol, MaxHR, Oldpeak) and categorical (Sex, ChestPainType, FastingBS, RestingECG, ExerciseAngina, ST_Slope).

Target Variable: The target is HeartDisease, a binary classifier (1 for disease, 0 for no disease).

Missing Data Handling: The notebook identifies that Cholesterol and RestingBP use 0 as a placeholder for missing data. These values are imputed by replacing them with the mean of the respective column (calculated after excluding the zeros).

Visualization: Various plots are used to understand the data:

Histograms for numerical feature distributions (Age, RestingBP, Cholesterol, MaxHR).

Count plots to show the relationship between categorical features (Sex, ChestPainType, FastingBS) and HeartDisease.

Box plots and violin plots to analyze feature distributions (e.g., Age and Cholesterol) against the target variable.

A correlation heatmap to show relationships between numerical features.

Data Preprocessing:

One-Hot Encoding: Categorical features (Sex, ChestPainType, RestingECG, ExerciseAngina, ST_Slope) are converted into numerical dummy variables using pd.get_dummies().

Train-Test Split: The data is split into an 80% training set and a 20% test set (random_state=42).

Feature Scaling: StandardScaler is fitted on the training data and used to transform both the training and test sets. This standardizes the feature ranges, which is crucial for models like KNN and SVC.

Model Training and Evaluation: Several classification models were trained and evaluated. The accuracy scores on the test set were as follows:

Logistic Regression: 87.0%

K-Nearest Neighbors (KNN): 87.0% (Note: The notebook trained KNN but used the Logistic Regression prediction variable for its accuracy printout. This accuracy reflects the KNN model.)

Support Vector Classifier (SVC): 84.8%

Gaussian Naive Bayes: 84.8%

Decision Tree Classifier: 78.8%

Cross-Validation: A 5-fold cross-validation was performed on the Gaussian Naive Bayes model, yielding a mean accuracy of 83.5%.
