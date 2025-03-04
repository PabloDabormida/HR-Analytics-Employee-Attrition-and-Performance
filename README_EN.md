# HR-Analytics-Employee-Attrition-and-Performance

🇪🇸 **Este proyecto está disponible en [Español](README.md)**  
<br>

📄 **Complete Documentation Available**

This Readme.md provides a summary of the analysis. To access the full documentation, including methodology, detailed analysis, insights, and final recommendations, check the following document:  
📎 **[Download Documentation (PDF)](https://github.com/PabloDabormida/HR-Analytics-Employee-Attrition-and-Performance/blob/main/Documentacion.pdf)**  
<br>

## 1. General Summary:
   
The objective of this report is to analyze employee attrition. Attrition is described as the gradual loss of employees over time. This phenomenon represents a significant problem for all organizations as it can impact staff, employee morale, project costs, loss of experience, and overall, an obstacle to organizational growth. We will examine the most important factors influencing attrition within an organization. We will consider whether these factors are within the organization’s control and what actions can be taken to mitigate or combat attrition. We will also analyze current trends in Human Resources and how they apply to our analysis; finally, based on our results, we will conclude with ideas and recommendations.  
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

## 3. General Data Description

The core of our analysis comes from a publicly available dataset, which provides variables similar to those that would typically be available to Human Resources personnel. This dataset can be found on Kaggle as "HR Analytics Employee Attrition & Performance" (Source: https://www.kaggle.com/datasets/mahmoudemadabdallah/hr-analytics-employee-attrition-and-performance). It consists of over 1,400 observations and 35 columns.  

The dataset includes a mix of numerical and categorical data types. Some examples of numerical data types include employee age, monthly income, and years working at the company. Examples of categorical variables include education, gender, job title, or the department in which the employee works. It is essential to verify the dataset’s structure and variable types, as data composition directly influences the nature of the analysis process.  
<br>

## 4. Data Processing
### 4.1. Conversion of the CSV file to a structured table
The analysis started from a CSV file. Although the file was identified as .csv, it had the .xls extension, which was corrected by opening it in Excel and saving it as an authentic .csv file. This ensured that the data could be correctly processed in Power BI.  
Subsequently, the file was converted into a structured table in Excel to facilitate data manipulation. This conversion allowed filters to be applied, data to be sorted, and operations to be performed on specific columns efficiently.  

### 4.2. Removal of unnecessary columns
The dataset columns were reviewed, and those that did not add direct value to the proposed analysis were removed. For example, irrelevant fields such as EmployeeCount, EmployeeNumber, or any data unrelated to performance or job satisfaction. This reduction of columns not only simplified the data model but also improved the performance of the analysis by reducing complexity.  

### 4.3. Duplicate verification
The data was reviewed to identify and eliminate duplicates in fields that should contain unique values, such as EmployeeID. This was necessary to ensure data integrity and avoid inconsistencies in the subsequent analysis.  

### 4.4. Creation of the "Performances" table
An independent table called "Performances" was designed, grouping all numerical data related to employee satisfaction and performance. This included indicators such as:  

• **JobSatisfaction**  
• **WorkLifeBalance**  
• **EnvironmentSatisfaction**  
• **RelationshipSatisfaction**  
• **WorkLifeBalance**  
• **JobInvolvement**  

This decision had several justifications:  

- **Standardization:** Centralizing all numerical indicators in a single table facilitates the visualization of performance metrics.  
- **Model optimization:** By separating quantitative data from descriptive ones, a clearer and more efficient structure for analysis in Power BI was created.  
- **Scalability:** It allows new performance-related metrics to be added in the future without modifying other tables.  

### 4.5. Creation of the PerformanceID field
To uniquely identify each record in the "Performances" table, a field called PerformanceID was generated. This field was constructed using a formula in Excel:  

**= "PR" & ROW() - ROW(1)**  

This formula generates a unique identifier for each row, with a format like PR1, PR2, ..., PR140. This not only allowed linking the "Performances" table with other tables in the model but also ensured the traceability of each record.  

The EmployeeID field was also added, which will be used to create the relationship with the "Employees" table.  

### 4.6. Creation of separate tables for specific indicators
Based on performance and satisfaction indicators, independent tables were created for each evaluated aspect, such as:  

• **JobSatisfaction:** Contains the descriptive levels of job satisfaction.  
• **EnvironmentSatisfactionLevel:** Defines the level of satisfaction with the work environment.  
• **WorkLifeBalanceLevel**: Classifies scores for work-life balance.  
• **RelationshipSatisfactionLevel:** Defines the level of satisfaction between the employee and the employer.  
• **PerformanceRating:** Describes the employee's rating based on their performance at work according to their manager.  
• **JobInvolvement:** Defines the employee's level of commitment to work.  

This approach had the following advantages:  

- **Readability:** By separating descriptive categories from numerical values, the model became more understandable.  
- **Flexibility:** It allows calculations and queries to be performed specifically for each indicator without affecting other metrics.  
- **Standardization:** Separate tables facilitate the reuse of descriptive categories in other analyses or reports.  

## 5. Scope
The analysis will include the collection, storage, and analysis of data related to performance (performance evaluations), satisfaction (satisfaction levels in various aspects), and the educational level of each employee. Factors such as work-life balance, seniority, and training opportunities will also be investigated. This analysis will help understand patterns and trends in employee development and satisfaction to make recommendations to improve performance and retain talent.  

#### **Strategic Level**
This analysis will enable organizational leaders to make informed decisions to:  

• Design retention strategies focused on high-performing employees and those at risk of leaving.  
• Identify critical areas affecting employee engagement, such as managerial management, the work environment, and development opportunities.  

#### **Tactical Level**
At a more operational level, the results of this analysis will help:

• Prioritize training and development initiatives based on areas where performance gaps are identified.  
• Optimize performance and satisfaction evaluation processes to ensure alignment with the organization's strategic objectives.  

#### **Operational Level**
Finally, the project will impact implementation in:  

• Creation of personalized training and mentoring programs.  
• Specific adjustments in work policies, such as hybrid schemes or support for employees with long commutes.  

## 6. Hypothesis
Employees with higher job satisfaction and work-life balance tend to stay longer in the company, reducing the attrition rate compared to those who report lower satisfaction in these aspects. This analysis will seek to evaluate the relationship between job satisfaction and turnover using multivariable analysis. Data will be segmented according to different departments, and logistic regression analysis will be conducted to identify the most influential factors in employee turnover. Additionally, patterns in seniority and promotions will be explored to determine their relationship with satisfaction and retention.  

## 7. Tools
• Excel for data reading, cleaning, and normalization.  
• PowerPoint for creating the mockup design.  
• Miro for creating the entity-relationship diagram (https://miro.com/).  
• Power BI for dashboard creation.  

## 8. Conclusions  

#### Critical Turnover Factors:  
• **Sales Representative:** This role has the highest turnover rate.  
• **Stock Option Level:** Employees at level 0 have significantly higher turnover (65% of those who left the company).  
• **OverTime:** Employees who work overtime have a much higher turnover rate (30.53%).  
• **Business Travel:** Employees who travel frequently have a turnover rate of 24.91%.  
• **Monthly Income:** More than 47% of employees who leave the company have salaries below $3,000.  


