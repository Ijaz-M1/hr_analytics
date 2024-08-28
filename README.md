# hr_analytics
 ![Screenshot 2024-08-28 113547](https://github.com/user-attachments/assets/1e65b15b-c723-4a9e-af05-b58e48a8d0b0)
 
 ![Screenshot 2024-08-28 113611](https://github.com/user-attachments/assets/bd4bad75-e2d0-47af-b71c-72e71236babc)
### Project workflow
#### Excel: Data Cleaning and Preparation

The first step involved downloading and cleaning the raw datasets. The datasets were created using ChatGPT with the aim to mirror real life HR datasets. I applied a series of best practices to ensure the data was accurate, consistent, and ready for deeper analysis:
- Standardised Data Formats: Ensured that all date fields were consistent (e.g., `DD/MM/YYYY` format), phone numbers followed a uniform pattern, and text data was consistently capitalised across all relevant columns.
- Duplicate Removal: Performed checks to identify and remove any duplicate records, ensuring that each employee was represented only once.
- Missing Data Handling: Checked for missing values, which ensured no significant gaps existed in important columns like salary, job title, or department.

This foundational step was critical to ensure the data’s integrity and reliability before moving forward to more complex analysis.

#### SQL Server Management Studio (SSMS): Data Integration and Querying

Once the data was cleaned, I uploaded three Excel files into SSMS, creating structured tables that were easy to work with:
- Table Setup: Designed the data tables with primary keys and relationships to ensure seamless joins and accurate data retrieval.
- Data Extraction Using SQL: Utilised `SELECT`, `FROM`, and `JOIN` queries to merge data from the three tables. This allowed me to create a more streamlined and focused dataset by selecting only the most relevant columns for analysis.
  ![Screenshot 2024-08-21 131128](https://github.com/user-attachments/assets/2ee7a193-89e3-41c0-8107-3f620adf2820)
- View Creation for Simplified Analysis: Built a SQL view that contained the refined dataset, aggregating key data points into a single source for analysis in Power BI. This step simplified the connection process and ensured consistent data availability.
  
  ![Screenshot 2024-08-21 131713](https://github.com/user-attachments/assets/0ae4efe7-aa3f-4436-a905-e9f00aa25b17)
- Data Quality Testing: To verify the integrity of the data, I implemented four key data quality checks.
  
  ![Screenshot 2024-08-21 152245](https://github.com/user-attachments/assets/684e7d79-2ac7-451b-99b1-63b12997656f)
  
  ![Screenshot 2024-08-21 144732](https://github.com/user-attachments/assets/2282145e-cf4b-4a5b-97bd-7c6924b091ca)
  ![Screenshot 2024-08-21 145156](https://github.com/user-attachments/assets/3e06c053-6bbc-4d57-972f-eb32a633346b)
  
  ![Screenshot 2024-08-21 150221](https://github.com/user-attachments/assets/c2db9218-603a-449d-9b33-db8126b6b126)
  ![Screenshot 2024-08-21 152120](https://github.com/user-attachments/assets/a15978e1-8f24-4dc9-b0b5-ee510bad57c9)

#### Power BI: Data Visualisation and Business Insights

With the data prepared and tested, I connected the SQL Server to Power BI to build insightful visualisations:
- Seamless Integration with SSMS: Connected Power BI directly to the SQL view created earlier, allowing for real-time data updates and efficient data retrieval.
- Interactive Visualisations: Developed six visualisations, each designed to answer business questions. These ranged from bar and column charts to line charts and treemaps, showcasing a variety of data storytelling techniques.
- DAX Formulas for Enhanced Analysis: Utilised DAX to create necessary columns and measures that enabled deeper insights. For example, I created a tenure calculation to analyse employee retention across departments.
- User-Friendly Dashboard: The final dashboard was designed to gain a comprehensive view of the HR data landscape.

#### Conclusion:
This project showcases the complete journey of transforming raw HR data into meaningful business insights. Starting with large Excel files containing varied employee information, I systematically cleaned and standardised the data, ensuring accuracy and consistency. Through the use of SQL Server Management Studio (SSMS), I integrated and refined the data, performing queries and creating views to streamline analysis. 
The final step involved connecting this processed data to Power BI, where I developed insightful visualisations tailored to answer key business questions. This project highlights my ability to manage the entire data analysis pipeline—from data cleaning and integration to advanced reporting and visualisation.

The information below will give a more in depth explanation into each visualisation.
### 1. Gender Pay Gap Analysis

**Business Question**: Is there a significant gender pay gap across different departments or job roles?

**Purpose**: The aim is to identify any disparities in pay between male and female employees within various job titles. Understanding this can help in promoting fair compensation practices.

**Insights**: The visualisation helps identify job roles where the gender pay gap is more pronounced. Any significant discrepancies between male and female average salaries may point to underlying issues in compensation policies, helping guide corrective actions.

### 2. Salary Analysis by Department
**Business Question**: What is the average salary per department, and how does it vary across departments?

**Purpose**: This analysis shows how salaries are distributed across departments. It helps HR and management assess which departments might be over or underpaid relative to others.

**Insights**: By comparing average salaries, the company can spot any departments where pay might need to be adjusted to align with industry standards or internal benchmarks. This can be a starting point for more detailed salary structure reviews.

### 3. Department Budget Utilisation

**Business Question**: What is the proportion of budget for each department?

**Purpose**: This analysis visualises the budget distribution across departments alongside the number of employees. 

**Insights**: The treemap reveals which departments have larger budgets and allows the business to act accordingly. 

### 4. Performance Rating by Location

**Business Question**: How do performance ratings vary by location?

**Purpose**: This chart helps identify any patterns in performance ratings across different office locations, which could inform HR strategies or uncover location-specific challenges.

**Insights**: This analysis shows how performance ratings are distributed across different locations. Locations with consistently lower ratings might require further investigation, such as understanding local management practices, employee engagement, or training needs.

### 5. Average Tenure by Department

**Business Question**: What is the average employee tenure by department?

**Purpose**: This chart helps visualise which departments retain employees for longer periods. It’s useful for understanding where employee satisfaction and retention might be highest or lowest.

**Insights**: Departments with longer average tenure often correlate with higher employee satisfaction or better management practices. Conversely, departments with short tenures might face retention issues, indicating areas for improvement in work culture or career development opportunities.

### 6. Hiring Trends: Employee Count by Year and Job Title

**Business Question**: What are the hiring trends by year and job title?
**Purpose**: This analysis shows hiring trends over time, giving insights into how the company’s workforce has grown and which job roles have been in demand. It’s essential for strategic workforce planning.
**Insights**: This visualisation reveals which job titles have seen the most growth, highlighting shifts in company priorities or market demands. It also shows periods of significant hiring spikes, which may align with business expansions or new project launches.

