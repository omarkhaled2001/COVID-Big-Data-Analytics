# 🦠 COVID-19 Big Data Analytics Project

**Cairo University | Computer Engineering Department | Spring 2024**  
Course: CMP4011 - Big Data and Cloud Computing

## 📖 Project Description

This project aims to analyze the mortality status of COVID-19 patients using big data techniques. By leveraging a large dataset of COVID-19 patients, we will develop a predictive model to determine which patients are at higher risk of mortality based on their symptoms. Additionally, association rules will be studied to find relationships between symptoms and underlying conditions, assisting in early diagnosis and better disease management.

## 🧠 Problem Statement

- **Objective**: Predict the mortality status (alive or deceased) of COVID-19 patients.
- **Analysis Goals**:
  - Study the co-occurrence of symptoms and underlying diseases.
  - Enable early intervention and disease management.
  - Develop a model that classifies patients based on their symptoms and other relevant factors.

## 📊 Dataset Information

- **Source**: [COVID-19 Dataset](https://www.kaggle.com/datasets/meirnizri/covid19-dataset)
- **Size**: 58.5 MB
- **Features**: 21 unique features
- **Records**: 1,048,576 unique patient entries
- **Provided by**: Mexican Government

## 🛠️ Tools & Technologies

- **Big Data Frameworks**: Hadoop (MapReduce), Spark
- **Programming Language**: Python
- **Cloud Computing**: Optional integration with AWS or Azure for distributed processing
- **Libraries Used**:
  - Data manipulation: `Pandas`
  - Visualization: `Matplotlib`, `Seaborn`
  - Machine Learning: `Scikit-learn`

## 🚀 Project Pipeline

1. **Data Preprocessing**:
   - Convert binary columns with values `97, 98, 99` to `NULL`.
   - Transform death dates into a binary value indicating death or survival.
   - Handle missing values by dropping columns with high null rates and rows with nulls.
2. **Exploratory Data Analysis (EDA)**:

   - Initial data analysis includes checking null percentages, plotting histograms, and checking correlations.
   - Identify outliers and explore feature importance using models like Random Forest and Decision Trees.

3. **Modeling**:

   - Split data into 80% training and 20% testing sets.
   - Train multiple models: Logistic Regression, Random Forest, Decision Trees, and Naive Bayes (MapReduce).

4. **Evaluation**:
   - Analyze model performance using metrics like accuracy, precision, recall, and F1 score.
   - Use only the most important 10 features to yield the best results.

## 📈 Key Insights

- There is significant **class imbalance** in the dataset.
- Patients with comorbidities such as **diabetes** or **asthma** have higher risk levels.
- **Male patients** have a higher death rate compared to females.
- **Older patients** are at a significantly higher risk.
- Hospitalized patients are more likely to pass away compared to those quarantined at home.

## 🎯 Model Results

| Model               | Dataset | Accuracy | Weighted Precision | Weighted Recall | Weighted F1 |
| ------------------- | ------- | -------- | ------------------ | --------------- | ----------- |
| Logistic Regression | Train   | 0.941    | 0.933              | 0.941           | 0.935       |
|                     | Test    | 0.941    | 0.932              | 0.941           | 0.935       |
| Random Forest       | Train   | 0.941    | 0.928              | 0.941           | 0.929       |
|                     | Test    | 0.939    | 0.926              | 0.939           | 0.927       |
| Decision Trees      | Train   | 0.940    | 0.927              | 0.940           | 0.927       |
|                     | Test    | 0.939    | 0.926              | 0.939           | 0.925       |
| Naive Bayes         | Train   | 0.921    | 0.945              | 0.921           | 0.930       |
|                     | Test    | 0.922    | 0.944              | 0.922           | 0.930       |

## 🛑 Unsuccessful Trials

- Imputing missing values for columns with high null percentages resulted in poor model performance.
- Feature importance techniques improved performance by dropping less significant columns.
- A Boolean classification feature didn't yield strong results; using a continuous measure may be more effective.

## 🚀 Future Work

- Test additional models, including **Neural Networks**.
- Further feature engineering to combine multiple features for better predictions.
- Conduct more **data mining** on the dataset to uncover hidden insights.

## 📝 How to Run

1. Clone this repository:
   ```bash
   git clone <repository_url>
   ```
2. Install dependencies:
   ```bash
   cd Code
   ```
3. To create dataset files used in the scripts

   ```bash
   python create-datasets.py
   ```

## ✨ Contributions

Feel free to submit **pull requests** for enhancements or suggestions! Contributions are always welcome.

## 📧 Contact

For any questions, reach out to the team at:

- **Team Members**:
  - Kareem Ashraf
  - Mahmoud Sief
  - Omar Khaled ALi
