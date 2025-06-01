BrewChill - Customer Satisfaction and Retention Analysis

This project focuses on understanding the key factors that influence customer satisfaction and retention for BrewChill Gold, a premium iced coffee product. The goal was to determine which attributes of the product—such as taste, packaging, and pricing—most significantly affect consumer behavior in terms of satisfaction, repurchase intention, and churn rate.

### What Was Done

The analysis followed a structured data science workflow:

1. Data Cleaning:
   - Handled missing values using mean, median, or mode based on skewness.
   - Replaced NaNs in categorical variables with 'No flavor' or the most frequent category.
   - Verified no duplicate rows were present.
   - Created a clean dataset ready for further analysis.

2. Exploratory Data Analysis (EDA):
   - Visualized distributions of key numerical variables (e.g., bitterness_level, sugar_pct, satisfaction).
   - Analyzed relationships between satisfaction and product features using scatter plots and bar charts.
   - Conducted statistical tests:
     - Spearman and Pearson correlations for numeric variables.
     - ANOVA and Kruskal-Wallis for categorical vs numeric comparisons.
     - Chi-square test to assess association between categorical variables like packaging_type and buy_again.

3. Predictive Modeling:
   - Built a regression model to predict customer satisfaction using variables such as bitterness_level, sugar_pct, aroma_strength, and price.
     - Achieved an R² score of 0.84 and a Mean Absolute Error (MAE) of 0.36.
   - Trained a classification model (Random Forest) to predict whether customers would buy again (`buy_again`).
     - Achieved an accuracy of 84%, with high recall and precision for both classes (Yes/No).

4. Feature Importance:
   - Identified the most influential features affecting satisfaction and purchase intention.
   - Highlighted opportunities to improve customer experience through product personalization and strategic changes.

---

### Key Findings

#### Factors Affecting Customer Satisfaction (`satisfaction`):

- **bitterness_level**: Strong negative correlation (-0.53). Higher bitterness reduces satisfaction.
- **sugar_pct**: Positive moderate correlation (+0.41). Increased sweetness improves customer experience.
- **aftertaste**: Positive moderate correlation (+0.46). Better aftertaste increases overall satisfaction.
- **aroma_strength**: Positive moderate correlation (+0.49). Stronger aroma enhances perceived quality.
- **churn_rate**: Strong negative correlation (-0.73). Lower churn means higher satisfaction.
- **discount_pct**: Positive moderate correlation (+0.39). Discounts can enhance perception of value.
- **price**: Weak positive correlation (+0.28). Customers associate higher prices with better quality.

#### Factors Influencing Repurchase Intention (`buy_again`):

- **satisfaction**: Strongest predictor. Satisfied customers are more likely to return.
- **price**: Moderate impact. Higher prices may indicate quality and increase loyalty.
- **packaging_type**: Sustainable packaging showed the highest satisfaction and slightly increased buy_again likelihood.
- **coffee_type** and **milk_type**: Statistically significant associations found using Chi-square tests. Certain combinations clearly lead to higher repurchase rates.

#### Statistical Insights:

- ANOVA/Kruskal-Wallis tests confirmed that `packaging_type`, `coffee_type`, and `milk_type` have a statistically significant impact on satisfaction.
- Chi-square tests revealed strong associations between `buy_again` and `coffee_type`, `milk_type`, and `packaging_type`.

#### Model Performance:

- **Regression Model (Predicting Satisfaction)**:
  - R² Score: 0.84
  - MAE: 0.36
  - Highly accurate in predicting satisfaction scores.

- **Classification Model (Predicting Buy Again)**:
  - Accuracy: 84%
  - Recall for "Yes" class: 83%
  - Precision for "Yes" class: 81%
  - Strong performance in identifying returning customers.

---

### What Can Be Predicted

From this analysis, we built two predictive models:

1. **Customer Satisfaction Regressor**:
   - Predicts satisfaction scores based on sensory attributes, economic factors, and packaging.
   - Useful for simulating how changes in formulation or pricing could affect customer perception.

2. **Repurchase Classifier**:
   - Predicts whether a customer will buy again based on their feedback and preferences.
   - Helps identify high-risk churn customers and personalize offerings to retain them.

---

### Business Implications for BrewChill

Based on the findings, here are some actionable recommendations:

- **Reduce bitterness level** in formulations to increase overall satisfaction.
- **Increase sugar percentage moderately**, especially for customers who prefer sweeter flavors.
- **Promote sustainable packaging**, as it has a clear positive effect on customer experience.
- **Offer almond or oat milk options**, as they show stronger associations with repurchase intent.
- Use the trained models to simulate new product configurations before launching them.
- Apply segmentation strategies based on customer profiles to improve targeting.

---

### Technologies Used

- Python
- Pandas, NumPy: Data manipulation
- Matplotlib, Seaborn: Data visualization
- Scikit-learn: Machine learning modeling
- SciPy, Statsmodels: Statistical testing
- Jupyter Notebook: Interactive analysis environment

---


### Authors

- william gutierrez – Data Analyst & Model Developer



### Future Steps

- Build an interactive dashboard using Plotly or Power BI.
- Deploy the predictive models in a web application for real-time simulation.


