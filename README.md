# Customer Churn Analysis for a Power Utility Company

This repository contains the analysis and predictive modeling conducted for a major gas and electricity utility that supplies energy to small and medium-sized enterprises. The objective was to identify drivers of customer churn and create a model to predict churn, enabling the company to take proactive measures to retain customers.

---

## Project Structure

The repository is organized into the following directories and files:

```
├── dataset/
│   ├── price_data.csv
│   ├── client_data.csv
│   ├── cleaned_data.csv
│   ├── out_of_sample_data_for_prediction.csv
│   ├── data_description.txt
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Feature_Engineering_Modeling_Prediction_Evaluation.ipynb
├── README.md
```

---

## Dataset

### Overview
The dataset folder contains multiple files, including:
1. **Price Data**: Contains information on energy prices for customers, including peak and off-peak prices.
2. **Client Data**: Contains customer information, including consumption, margins, tenure, and churn status.
3. **Cleaned Data**: The dataset prepared after exploratory data analysis (EDA).
4. **Out-of-Sample Data**: A dataset for testing the model on unseen data.
5. **Data Description File**: Detailed metadata on the columns in the datasets.

---

## Notebooks

### 1. Exploratory Data Analysis (EDA)
The first notebook explores the dataset in-depth:
- **Descriptive Analysis**: Summary statistics of key features.
- **Data Visualization**:
  - Distribution of numerical features such as `cons_12m`, `forecast_cons_12m`, `net_margin`, etc.
  - Churn analysis by sales and churn channels.
  - Correlation heatmaps to explore relationships between variables.
- **Key Insights**:
  - Consumption and margins vary widely across customers.
  - Price sensitivity appears to influence churn behavior.
  - Strong correlation between certain variables, such as historical and recent consumption.
- **Hypothesis Testing**:
  - Explored the relationship between price sensitivity and churn using visualizations such as box plots.

### 2. Feature Engineering, Modeling, and Evaluation
The second notebook covers:
- **Feature Engineering**:
  - Created new features to improve model performance (e.g., tenure, contract update frequency, price sensitivity metrics).
  - Transformed categorical and numerical variables for modeling.
- **Modeling**:
  - A `Random Forest Classifier` was used for prediction. Random Forest is an ensemble learning method that leverages the collective decision of multiple decision trees for robust performance.
- **Evaluation**:
  - Metrics: 
    - **Accuracy**: `90.36%`
    - **Precision**: `81.82%`
    - **Recall**: `4.92%`
  - Feature importance analysis highlighted:
    - Top drivers of churn: net margin, 12-month consumption, margin on power subscriptions, and tenure.
    - Price sensitivity is a weak contributor to churn prediction.

### Bonus Strategy Analysis
- **Proposed Strategy**: Offered a 20% discount to customers with a high propensity to churn.
- **Result**: Presented findings to senior stakeholders to evaluate potential retention strategies.

---

## Key Findings

### EDA Insights
1. **Consumption and Margin Trends**:
   - Most customers exhibit lower consumption, with a minority having significantly higher energy usage.
   - Net margin varies widely, reflecting differences in customer profitability.
2. **Churn Behavior**:
   - Customers with higher price sensitivity tend to churn more frequently.
3. **Correlation Analysis**:
   - Strong correlation between historical and recent consumption metrics.
   - Relationship between gross and net margins on power subscriptions.

### Modeling Insights
1. **Drivers of Churn**:
   - Net margin and consumption over 12 months are the strongest predictors of churn.
   - Tenure and contract update frequency significantly influence churn likelihood.
   - Price sensitivity plays a minor but notable role in customer churn.

2. **Hypothesis Testing**:
   - Price sensitivity is not the primary driver of churn but is a weak contributor.
![output](https://github.com/user-attachments/assets/5e436dc9-a506-44be-8691-2f5677a02c2a)

---

## Tools & Technologies
- **Python**: For data analysis, modeling, and evaluation.
- **Libraries**:
  - `Pandas`, `NumPy`: Data manipulation and analysis.
  - `Matplotlib`, `Seaborn`,`Plotly`: Data visualization.
  - `Scikit-learn`: Machine learning and evaluation.

---

## Future Work
- Conduct further experiments to refine the hypothesis on price sensitivity.
- Explore advanced modeling techniques to improve recall while maintaining precision.
- Evaluate the effectiveness of the proposed discount strategy using a simulated environment or A/B testing.

---

## How to Use

### Prerequisites
- Python 3.8+ installed
- Required libraries (`requirements.txt` not included but can be generated based on the libraries used above)

### Steps
1. Clone this repository:
   ```
   git clone https://github.com/Sudhanshu1st/Customer-Churn-Analysis.git
   cd customer-churn-analysis
   ```
2. Access the datasets in the `dataset/` folder.
3. Open the notebooks in the `notebooks/` folder to explore EDA and run the model.
4. Use the cleaned data or `out_of_sample_data_for_prediction.csv` to test the model.
