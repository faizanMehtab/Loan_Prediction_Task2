🏦 Task 2: Loan Approval Prediction
📌 Objective

The objective of this task is to predict whether a loan application will be approved or not based on applicant details such as income, education, credit history, and property area. This helps financial institutions make data-driven lending decisions.

📊 Dataset Description

The dataset contains 614 loan applications with the following key features:

Demographic Features: Gender, Married, Dependents, Education, Self_Employed

Financial Features: ApplicantIncome, CoapplicantIncome, LoanAmount

Loan Details: Loan_Amount_Term, Credit_History, Property_Area

Target Variable:

Loan_Status → Y (Approved), N (Not Approved)

🧹 Data Cleaning & Preparation

Missing values in numerical columns were filled using the mean.

Missing values in categorical columns were filled using the mode.

Categorical variables were converted into numeric format using Label Encoding.

Loan_ID was removed as it does not contribute to prediction.

📈 Exploratory Data Analysis (EDA)

The following visualizations were performed:

Scatter plot of Applicant Income vs Loan Amount by Loan Status

Count plot of Education vs Loan Status

Histogram of Applicant Income

Box plot of Loan Amount vs Loan Status

Key Observations:

Applicants with higher income are more likely to get loan approval.

Graduates have a higher loan approval rate.

Loan amount distribution varies significantly between approved and non-approved loans.

🤖 Model Used

Logistic Regression

Solver: lbfgs

Regularization: L2

Maximum iterations: 5000

Train-test split: 70% training / 30% testing

📊 Model Evaluation

Accuracy: ~78%

Confusion Matrix:

	Predicted No	Predicted Yes
Actual No	27	38
Actual Yes	2	118
Interpretation:

The model correctly predicts most approved loans.

Very few false negatives, meaning eligible applicants are rarely rejected.

Some false positives, where loans were predicted approved but were not.

📌 Conclusion & Business Insights

Credit History, Applicant Income, and Education level are strong indicators of loan approval.

Logistic Regression performed well and is suitable for this binary classification task.

The model can help banks reduce risk while approving loans efficiently.

🛠 Tools & Technologies

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Jupyter Notebook