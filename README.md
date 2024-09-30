Churn Analysis and Rediction on  WA_Fn-UseC_-Telco-Customer-Churn.csv

##A streamlit Dashboard 
![image](https://github.com/user-attachments/assets/4d765efb-7971-4fd2-a531-8ca076fc6211)

1. **Dashboard Styling**:
   - Custom styles using `st.markdown` for hover effects, headings, and animation.
   - A key feature is the dynamic title using the `hover-effect` and `change_content` class, which changes based on different aspects of churn analysis.

2. **Sidebar Controls**:
   - You’ve used Streamlit's sidebar to allow users to select different customer features to explore their relationship with churn.
   - There are three main levels of selection for analyzing churn relations using Plotly bar charts.
![image](https://github.com/user-attachments/assets/a84d1271-c6ef-4d78-99f4-c682a0304a06)

3. **Logistic Regression Model**:
   - The script has a section to perform logistic regression on the churn data.
   - Label encoding is used to convert categorical features, followed by training and evaluation using a logistic regression model.
   - A confusion matrix is plotted using Plotly's heatmap.

4. **Gender Distribution & Churn**:
   - Pie charts show the distribution of male and female customers, as well as churn vs. non-churn customers.

5. **Customer Analysis Based on Attributes**:
   - Bar plots showing customer distribution based on attributes like `SeniorCitizen`, `Dependents`, and `Partner` are created using both `plotly.express` and `plotly.graph_objects`.

6. **Loyalty vs. New Customers**:
   - Customers are divided into `loyal` (tenure ≥ 12 months) and `new` (tenure < 12 months), with bar charts visualizing their distribution by gender.

7. **Churn Analysis**:
   - You’ve included churn analysis based on customer loyalty and contract type, showing how churn varies across different groups.

### Suggested Improvements:

- **Improve Code Reusability**: You can refactor the repeated sections of code (like loading data and encoding features) into functions to improve readability and maintainability.
  
- **Dynamic Label Handling**: For the dynamic content like `hover-effect` and `change_content`, you might want to parameterize these so that they can be reused in multiple sections without hardcoding the HTML repeatedly.

- **Data Validation**: You might consider adding more data validation steps (e.g., handling missing values) before training the logistic regression model.

