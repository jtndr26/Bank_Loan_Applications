
# Bank Loan Application
 - Exploratory Data Analysis



## Authors

- [Jeetendra Sarpe](https://github.com/jtndr26)


### Business Context:
In the competitive banking sector, efficient loan processing is essential for maintaining customer satisfaction and profitability. However, traditional methods of assessing loan applications often lack precision, leading to inefficiencies and potential risks for the bank. To address this challenge, banks are increasingly turning to data-driven approaches, leveraging advanced analytics and machine learning algorithms to improve loan approval processes. By analyzing historical data and identifying patterns in loan applicant profiles, banks can make more accurate and timely decisions, mitigating risks and maximizing returns on their loan portfolios. This project aims to enhance loan application processing by employing exploratory data analysis (EDA) techniques to identify key factors influencing loan approvals, thereby streamlining the decision-making process and ensuring fair and efficient allocation of funds.

### Project Description:
Utilizing exploratory data analysis (EDA), this project aims to uncover patterns within the dataset to ensure that loan applicants capable of repaying are not unfairly rejected. The analysis begins with a presentation outlining the problem statement and our approach. Missing data is identified and addressed using appropriate methods. Results from univariate, segmented univariate, and bivariate analyses are interpreted in business terms to provide actionable insights. Furthermore, the top 10 correlations for clients with payment difficulties and all other cases (the target variable) are identified, with visualizations and summaries provided to highlight key findings and their significance in differentiating clients with payment difficulties.
### Data Overview:

https://drive.google.com/drive/u/0/folders/1dNzwBjyMg9gLgXKYzQGg-6Iewfn0fm2L

The dataset consists of multiple tables containing various attributes related to loan applications and previous application data. Attributes include demographic information such as gender, age, and family status, financial details such as income, credit amount, and annuity, as well as application-related variables like contract type, ownership status, and applicant's occupation. Additionally, there are features indicating previous application details such as contract status, payment type, and goods category. The dataset also includes variables related to applicant behavior, such as days since last phone change and flag for email and phone contact. Moreover, there are columns indicating the presence of documents and requests for credit bureau inquiries.

The provided data appears to be related to loan applications, with various attributes describing both the applicants and their previous credit history. Here's a brief overview of the data:

### application_data:
- **SK_ID_CURR**: ID of the loan application in the sample.
- **TARGET**: Target variable indicating if the applicant had payment difficulties.
- **NAME_CONTRACT_TYPE**: Type of loan contract (cash or revolving).
- **CODE_GENDER**: Gender of the applicant.
- **FLAG_OWN_CAR**: Flag indicating if the applicant owns a car.
- **FLAG_OWN_REALTY**: Flag indicating if the applicant owns real estate.
- **CNT_CHILDREN**: Number of children the applicant has.
- **AMT_INCOME_TOTAL**: Total income of the applicant.
- **AMT_CREDIT**: Amount of credit requested by the applicant.
- **AMT_ANNUITY**: Loan annuity.
- **AMT_GOODS_PRICE**: Price of goods for which the loan is given.
- **NAME_TYPE_SUITE**: Who was accompanying the client when applying for the loan.
- **NAME_INCOME_TYPE**: Type of income of the applicant (e.g., working, maternity leave).
- **NAME_EDUCATION_TYPE**: Highest education level of the applicant.
- **NAME_FAMILY_STATUS**: Family status of the applicant.
- **NAME_HOUSING_TYPE**: Housing situation of the applicant.
- **REGION_POPULATION_RELATIVE**: Normalized population of the region where the applicant lives.
- **DAYS_BIRTH**: Age of the applicant in days at the time of application.
- **DAYS_EMPLOYED**: Number of days before the application the applicant started current employment.
- **...** (and many more attributes)

### previous_application.csv:
- **SK_ID_PREV**: ID of the previous credit in Home Credit related to a loan in the sample.
- **SK_ID_CURR**: ID of the loan in the sample.
- **NAME_CONTRACT_TYPE**: Type of contract product of the previous application.
- **AMT_ANNUITY**: Annuity of the previous application.
- **AMT_APPLICATION**: Amount of credit requested in the previous application.
- **AMT_CREDIT**: Final credit amount in the previous application.
- **...** (and many more attributes)

The data contains a mix of categorical and numerical features, along with some time-related attributes. It seems suitable for building predictive models to assess credit risk or analyze customer behavior in loan applications. Additionally, there are normalized scores and flags indicating various aspects such as document provision and social surroundings.
## Approach

Exploratory Data Analysis (EDA) is crucial for understanding the underlying patterns, relationships, and characteristics of the data before diving into modeling. Here's an approach for conducting EDA on the provided datasets:

1. **Data Loading and Inspection**:
   - Load the datasets into your environment (e.g., Python using pandas).
   - Inspect the first few rows of each dataset to understand its structure and the type of data present.
   - Check the data types of each column and handle any inconsistencies.

2. **Data Cleaning and Preprocessing**:
   - Handle missing values: Identify missing values in each dataset and decide on appropriate strategies for handling them (e.g., imputation, deletion).
   - Handle outliers: Identify outliers in numerical features and decide whether to remove or transform them.
   - Encode categorical variables: Convert categorical variables into numerical representations using techniques like one-hot encoding or label encoding.
   - Normalize or scale numerical features if necessary to ensure they are on a similar scale.

3. **Univariate Analysis**:
   - Explore each variable individually:
     - For numerical variables: Plot histograms, box plots, or density plots to understand the distribution, central tendency, and spread of the data.
     - For categorical variables: Plot bar plots to visualize the frequency distribution of categories.
   - Compute summary statistics such as mean, median, mode, standard deviation, etc., for numerical variables.

4. **Bivariate Analysis**:
   - Explore relationships between pairs of variables:
     - For numerical vs. numerical variables: Plot scatter plots or correlation matrices to identify any linear relationships.
     - For categorical vs. numerical variables: Plot box plots or violin plots to compare distributions across categories.
     - For categorical vs. categorical variables: Create contingency tables and visualize them using heatmaps or stacked bar plots.

5. **Feature Engineering**:
   - Create new features that may be useful for modeling based on domain knowledge or insights gained during EDA.
   - Extract additional information from date or time-related variables if applicable.

6. **Multivariate Analysis**:
   - Explore interactions and relationships among multiple variables simultaneously:
     - Use techniques like pair plots, heatmaps, or parallel coordinates plots to visualize interactions between multiple variables.
     - Conduct hypothesis testing or ANOVA to assess the significance of relationships.

7. **Data Visualization**:
   - Utilize various visualization techniques such as seaborn, matplotlib, or plotly to create informative plots and charts.
   - Create visual summaries and insights that effectively communicate findings to stakeholders.

8. **Summary and Insights**:
   - Summarize key findings, patterns, and insights discovered during the EDA process.
   - Document any assumptions made, data transformations performed, and decisions taken during the analysis.
   - Identify potential challenges or limitations in the data that may impact subsequent modeling efforts.

9. **Iterative Process**:
   - EDA is often an iterative process, so revisit earlier steps as needed based on new insights or questions that arise during the analysis.
   - Collaborate with domain experts or stakeholders to validate findings and ensure alignment with business objectives.



## **Result**: 

Based on the insights provided, here are the corresponding results from the EDA:

1. **Gender Distribution**:
   - Female applicants significantly outnumber male applicants in the dataset.

2. **Education Level**:
   - Majority of applicants have a Secondary/Secondary Special education level.

3. **Occupation**:
   - Laborers constitute a significant portion of the applicant occupation types.

4. **Previous Application Status**:
   - Most previous applications were approved.

5. **Utilization of Approved Offers**:
   - A large majority of applicants use the loan offer once it's approved.

6. **Income Level**:
   - Majority of applicants belong to the low-income group, indicating income as a crucial factor in loan approval.

7. **Property Ownership**:
   - Most applicants own property, suggesting property ownership as a potential factor in loan approval.

8. **Income and Occupation**:
   - Managers typically have higher incomes compared to other occupation types.

9. **Income Disparities**:
   - Cooking/Cleaning Staff and Low-skill Laborers are among the low-income groups.

10. **Education and Income**:
    - Applicants with academic degrees tend to have higher incomes, potentially increasing their chances of loan repayment.

11. **Repayment Probability**:
    - Single low-skilled laborers and widows in HR-Staff and Driver occupations have the highest chance of loan repayment.

12. **Targeted Occupation**:
    - Low-skill laborers are highly targeted in general, possibly due to their lower income levels.

These insights provide valuable information for understanding the demographics, socio-economic factors, and occupation-related characteristics of loan applicants. They can help in refining the loan approval process and identifying risk factors associated with defaulting on loans.

![image](https://github.com/jtndr26/Bank_Loan_Applications/assets/78334379/3669c752-cd7f-4218-b8d4-d894c6a88049)
![image](https://github.com/jtndr26/Bank_Loan_Applications/assets/78334379/8af5d36e-c7c8-4a65-81d1-529fd9044320)

![image](https://github.com/jtndr26/Bank_Loan_Applications/assets/78334379/5ec2c55f-0735-4cb9-94f6-9a9981fd1421)

## **Conclusion**:
The exploratory data analysis (EDA) of the provided datasets offers valuable insights into the demographics, socio-economic attributes, and occupational profiles of loan applicants. The gender distribution indicates a significant predominance of female applicants, suggesting potential gender-specific trends in loan application behavior. Education level analysis reveals that a large proportion of applicants have attained a Secondary/Secondary Special education, highlighting the need for tailored financial products and services for individuals with varying educational backgrounds.

Occupationally, laborers emerge as a predominant group among applicants, underscoring the importance of understanding the income dynamics and stability within this occupation category. The majority of previous applications being approved implies a relatively favorable lending environment, but further analysis is warranted to assess the factors influencing approval decisions and their impact on loan performance.

The utilization of approved offers by a vast majority of applicants indicates a high demand for credit facilities, which aligns with the observed prevalence of low-income applicants. Income emerges as a critical determinant in loan approval, with disparities evident across different occupation types. While managers typically exhibit higher incomes, low-skilled laborers and cooking/cleaning staff face financial challenges, potentially affecting their repayment capacity.

Education emerges as a significant predictor of income level, with applicants holding academic degrees generally enjoying higher incomes. This finding underscores the importance of educational attainment in fostering financial stability and loan repayment capability. Furthermore, specific occupation categories, such as single low-skilled laborers and widows in HR-Staff and Driver roles, exhibit a higher likelihood of loan repayment, suggesting potential risk mitigation strategies for lenders.

Overall, the EDA underscores the complexity of factors influencing loan approval and repayment behavior. By leveraging these insights, financial institutions can refine their credit assessment processes, tailor product offerings to meet diverse customer needs, and mitigate risks associated with default. Additionally, targeted interventions aimed at supporting financially vulnerable groups can promote financial inclusion and responsible lending practices, ultimately fostering economic empowerment and stability within the community.isition.





