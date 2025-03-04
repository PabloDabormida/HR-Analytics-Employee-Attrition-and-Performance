# HR-Analytics-Employee-Attrition-and-Performance

🇪🇸 **Este proyecto está disponible en [Español](README.md)**  
<br>

📄 **Complete Documentation Available**

This Readme.md provides a summary of the analysis. To access the full documentation, including methodology, detailed analysis, insights, and final recommendations, check the following document:  
📎 **[Download Documentation (PDF)](https://github.com/PabloDabormida/HR-Analytics-Employee-Attrition-and-Performance/blob/main/Documentacion.pdf)**  
<br>
<br>

## 1. General Summary:
   
The objective of this report is to analyze employee attrition. Attrition is described as the gradual loss of employees over time. This phenomenon represents a significant problem for all organizations as it can impact staff, employee morale, project costs, loss of experience, and overall, an obstacle to organizational growth. We will examine the most important factors influencing attrition within an organization. We will consider whether these factors are within the organization’s control and what actions can be taken to mitigate or combat attrition. We will also analyze current trends in Human Resources and how they apply to our analysis; finally, based on our results, we will conclude with ideas and recommendations.  
<br>
<br>

## 2. Introduction:
   
Human capital is one of the greatest assets an organization can have. Companies can spend up to 70% of total business costs on employees. These costs include salaries, training, recruitment, and skill investments. Additionally, recruiting and retaining top talent is essential for long-term growth and sustainability. Employees often possess key characteristics that are instrumental in driving the company forward. Knowing this, when employees decide to resign or leave a company, it can become a serious problem. With each employee departure, the company loses its direct investment along with all the knowledge and experience the employee would have inherently provided. In the field of Human Resources, when employees decide to leave the company, this is known as employee attrition, and this is the focus of our analysis.  

By analyzing the causes of attrition, we find overlapping evidence of why employees decide to leave, where in most cases, it is due to the following reasons: unsatisfactory compensation, unsatisfactory benefits, lack of growth or development opportunities, work-life balance issues, poor management, poor working conditions, and lack of recognition for work achievements or added value in the workplace.  

In this report, we will analyze the validity of these reasons through a thorough analysis of a publicly available employee dataset. Our approach will follow a set of procedures, which include: research, exploratory data analysis, data manipulation and cleaning, model preparation, model building and evaluation, and finally, data visualization and analysis using Power BI.  

• **Initial Research:** We will start with a review of the dataset to understand its structure, available variables, and relevance to the analysis objectives. This stage is crucial to defining the project’s scope and anticipating possible challenges.  

• **Data Manipulation and Cleaning:** Next, we will clean the dataset by addressing missing values, duplicates, and errors. This step ensures the data is reliable and ready for further analysis.  

• **Data Normalization:** Once the data is clean, we will normalize it to ensure it is in a suitable format for modeling. This includes transforming variables and encoding categorical data.  

• **Relational Model Construction:** After normalization, we will design the relational model, creating an entity-relationship (ER) diagram that represents relationships between different entities in the dataset. This provides a strong foundation for structured queries and detailed analysis.  

• **Exploratory Data Analysis (EDA):** A preliminary descriptive analysis is conducted to identify patterns, trends, and anomalies in the data. By using basic visualizations, we gain an initial understanding of key relationships between variables.  

• **Data Analysis and Visualization:** Finally, we will conduct a detailed analysis using the relational model as a guide, and we will use Power BI to create interactive visualizations that highlight key patterns and facilitate result interpretation. This allows us to present key findings clearly and effectively.  
<br>
<br>

## 3. General Data Description

The core of our analysis comes from a publicly available dataset, which provides variables similar to those that would typically be available to Human Resources personnel. This dataset can be found on Kaggle as "HR Analytics Employee Attrition & Performance" (Source: https://www.kaggle.com/datasets/mahmoudemadabdallah/hr-analytics-employee-attrition-and-performance). It consists of over 1,400 observations and 35 columns.  

The dataset includes a mix of numerical and categorical data types. Some examples of numerical data types include employee age, monthly income, and years working at the company. Examples of categorical variables include education, gender, job title, or the department in which the employee works. It is essential to verify the dataset’s structure and variable types, as data composition directly influences the nature of the analysis process.  
<br>
<br>

## 4. Data Processing

To ensure the accuracy and reliability of the data used in our analysis, we performed the following data processing steps:

- **Handling Missing Values:** We identified and managed missing values through appropriate techniques such as imputation or removal, depending on the context of the variable.  
- **Data Cleaning:** We eliminated duplicate records, standardized formats, and corrected inconsistencies in categorical variables.  
- **Data Transformation:** Certain variables were transformed to ensure consistency and improve interpretability. For instance, categorical variables were encoded into numerical values where necessary.  
- **Feature Engineering:** We created new variables based on existing data to extract more relevant insights.  

## 5. Scope  

The analysis includes the collection, storage, and examination of data related to employee performance (performance evaluations), satisfaction (levels of satisfaction in various aspects), and educational background. Additionally, factors such as work-life balance, tenure, and training opportunities will be explored. This analysis aims to identify patterns and trends in employee development and satisfaction, providing recommendations to improve performance and retain talent.  

### **Strategic Level**  

This analysis will enable organizational leaders to make informed decisions to:  

- Design retention strategies focused on high-performing employees and those at risk of leaving.  
- Identify critical areas affecting employee engagement, such as managerial leadership, work environment, and development opportunities.  

### **Tactical Level**  

At a more operational level, the results of this analysis will serve to:  

- Prioritize training and development initiatives based on identified performance gaps.  
- Optimize performance and satisfaction evaluation processes to align them with the organization’s strategic goals.  

### **Operational Level**  

Finally, this project will impact implementation by:  

- Creating personalized training and mentoring programs.  
- Making specific policy adjustments, such as hybrid work schemes or support for employees with long commutes.  

## 6. Hypothesis  

We formulated the following hypotheses regarding employee attrition:  

1. Salary dissatisfaction significantly increases the likelihood of employee attrition.  
2. Lack of career growth opportunities is one of the main drivers of employee turnover.  
3. Work-life balance issues contribute to higher attrition rates.  
4. Employees with higher job satisfaction are less likely to leave the company.  

## 7. Tools  

To conduct this analysis, we used various tools, including:  

- **Python** for data processing and exploratory analysis.  
- **Pandas & NumPy** for data manipulation.  
- **Matplotlib & Seaborn** for data visualization.  
- **Power BI** for interactive dashboards.  

## 8. Conclusions  

The findings from this analysis provide valuable insights into employee attrition. Some key conclusions include:  

- Employees with lower compensation and fewer career development opportunities are more likely to leave.  
- Job satisfaction plays a crucial role in retention.  
- Implementing employee recognition programs can help improve retention rates.  

## 📊 **Explore the complete interactive dashboard**  
📎 **[View Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYzNkZDFlN2EtZTY1Zi00NDQ1LTgyYmMtYmQ5NGNjZDM1MTg4IiwidCI6IjY1NDhkYzM4LWVkMTAtNGJiZC05NTZmLTVlNTM3NzVkYmI5ZCIsImMiOjR9)**  

## 9. Recommendations  

Based on the analysis, the following recommendations are suggested to reduce employee attrition:  

- **Increase Compensation & Benefits:** Conduct regular salary benchmarking to ensure employees are competitively compensated.  
- **Career Development Programs:** Provide growth opportunities through training, mentorship, and internal promotions.  
- **Improve Work-Life Balance:** Introduce flexible work arrangements and wellness programs.  
- **Enhance Employee Recognition:** Implement reward and recognition programs to boost job satisfaction.  

---  
📄 **For a detailed analysis, access the full report.**  
📎 **[Download Documentation (PDF)](https://github.com/PabloDabormida/HR-Analytics-Employee-Attrition-and-Performance/blob/main/Documentacion.pdf)**  

