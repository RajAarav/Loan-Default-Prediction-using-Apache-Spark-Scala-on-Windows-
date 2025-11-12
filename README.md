Loan Default Prediction Using Apache Spark

This project predicts the probability of loan default using financial and demographic data. It demonstrates how big data tools like Apache Spark can be used for scalable data preprocessing, model training, and evaluation.

📊 Project Overview

The goal is to analyze loan applicant data and predict whether a person is likely to default on their loan. Logistic Regression was used as the classification model after encoding categorical variables and scaling numeric features.

⚙️ Technologies Used

    Apache Spark (Scala on Spark Shell)

    Spark MLlib

    Kaggle Loan Dataset (cleaned and customized)

    Windows Environment

🧩 Steps Performed

    Loaded the dataset into a Spark DataFrame

    Encoded categorical variables and scaled numerical ones

    Trained a Logistic Regression model to classify default risk

    Evaluated model performance using a Confusion Matrix and Accuracy Score

    Stored prediction results in Spark SQL and saved them as CSV

    Visualized default probabilities using a simple dashboard

⚙️ How It Was Done

    Downloaded a loan dataset from Kaggle and saved it as loan_data_large.csv.

    Opened Spark Shell in CMD and loaded the dataset using:

    val loanDF = spark.read.option("header","true").option("inferSchema","true").csv("path")

    Encoded categorical columns and scaled numerical ones using StringIndexer, OneHotEncoder, and StandardScaler.

    Trained a Logistic Regression model to predict the default column.

    Evaluated the model using a confusion matrix and accuracy metrics.

    Saved the final predictions as CSV to the given output path.

📈 Results

The model successfully classified loan defaults with good accuracy. The output predictions and probabilities were stored for further analysis and visualization.
🚀 Future Scope

    Use Random Forest or Gradient Boosting for higher accuracy

    Deploy the model using PySpark or Streamlit for real-time scoring

    Integrate more financial variables for deeper insights
