<!DOCTYPE html>
<html>
<body>
    <h1>LoanTap Creditworthiness Prediction Project</h1>
  
<h2>Overview</h2>
<p>
    LoanTap is a digital lending platform targeting millennials and salaried professionals with customized credit offerings like personal loans, EMI-free loans, and salary advances. To scale operations while maintaining credit quality, LoanTap aims to develop a data-driven underwriting model that predicts whether an applicant will fully repay their personal loan or default (charged off), using historical loan and borrower data.
</p>

<h2>Key Objectives</h2>
<ul>
    <li>Build an interpretable classification model to predict loan default risk.</li>
    <li>Use historical data to derive insights into borrower behavior and creditworthiness.</li>
    <li>Engineer features that enhance model performance and reduce risk exposure.</li>
    <li>Translate model findings into actionable business recommendations for LoanTap.</li>
</ul>

<h2>Methodology</h2>
<ul>
    <li>Exploratory data analysis and feature transformation on 396,030 loan records.</li>
    <li>Feature engineering: log transformation, capping outliers, imputation, and encoding.</li>
    <li>Modeling via Logistic Regression with SMOTE for class balancing and GridSearchCV for hyperparameter tuning.</li>
    <li>Evaluation using metrics such as ROC AUC, Precision-Recall AUC, and VIF for multicollinearity.</li>
</ul>

<h2>Key Insights</h2>
<ul>
    <li>Approximately 80.4% of loans were fully paid, while 19.6% were charged off.</li>
    <li>Sub-grade and interest rate had a strong positive correlation (r = 0.97).</li>
    <li>Loan amount and installment were highly correlated (r = 0.95).</li>
    <li>Applicants from ZIP codes 00813, 29597, and 05113 had 100% full repayment; ZIP codes 11650, 93700, and 86630 had 100% defaults.</li>
    <li>The highest observed DTI was 9999; values were capped at 100 to remove extreme outliers.</li>
    <li>Log transformation of annual income reduced skewness from 41.04 to 0.16.</li>
    <li>Precision-Recall AUC of the final logistic model exceeded 0.75; ROC AUC was around 0.80.</li>
</ul>

<h2>Recommendations</h2>
<ul>
    <li>Deploy the logistic regression model to automate credit decisions for personal loans.</li>
    <li>Apply higher scrutiny or rejection criteria for applicants with high sub-grade (e.g., G5) and high interest rates.</li>
    <li>Incorporate ZIP code and credit history length as risk flags for underwriting decisions.</li>
    <li>Continuously monitor and retrain the model every 6–12 months with updated loan data.</li>
</ul>
</body>
</html>
