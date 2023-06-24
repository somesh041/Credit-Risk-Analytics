# Credit-Risk-Analytics

## Project Overview
The primary objective of this case study is to detect specific patterns that serve as indicators of clients experiencing challenges in making their installment payments. These patterns can then be utilized to determine appropriate actions, including denying the loan, decreasing the loan amount, or granting loans to applicants with higher risk profiles but at elevated interest rates. By implementing these measures, the aim is to ensure that deserving borrowers capable of repaying their loans are not unfairly turned down. In essence, the study aims to create a comprehensive understanding of the characteristics associated with clients who may face payment difficulties, enabling more informed lending decisions while safeguarding the interests of responsible borrowers.

## Table Of Contents
* Business Understanding
* Data Understanding
* Data Cleaning
* Data Analysis
* Insights and Conclusion
## Business Understanding

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

 1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

2. If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

The data given below contains the information about the loan application at the time of applying for the loan. It contains two types of scenarios:

1. The client with payment difficulties: he/she had late payment more than X days on at least one of the first Y instalments of the loan in our sample,

2. All other cases: All other cases when the payment is paid on time.

When a client applies for a loan, there are four types of decisions that could be taken by the client/company):

1. Approved: The Company has approved loan Application

2. Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan or in some cases due to a higher risk of the client he received worse pricing which he did not want.

3. Refused: The company had rejected the loan (because the client does not meet their requirements etc.).

4. Unused offer: Loan has been cancelled by the client but on different stages of the process.

In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.
## Data Understanding

This dataset has 3 files as explained below:
1. 'application_data.csv' contains all the information of the client at the time of application.
* The data is about whether a client has payment difficulties.
2. 'previous_application.csv' contains information about the client’s previous loan data. 
* It contains the data on whether the previous application had been Approved, Cancelled, Refused or Unused offer.
3. 'columns_description.csv' is data dictionary which describes the meaning of the variables.
* Description of the variables.

Datasets link : https://drive.google.com/drive/folders/1DOnkn5m8CLCiwZggF4d6fe9K_RQaHqMs?usp=sharing



## Data Cleaning

### Handling Missing Values
* Highly missing value features were dropped, followed by descriptive statistics-based removal of imbalanced and insignificant variable.
* Numerical data type had 47 features with more than 40% missing data.
Missing data was examined for patterns of Missing Completely At Random (MCAR), Missing At Random (MAR), and Missing Not At Random (MNAR). Through meticulous analysis of descriptive statistics, irrelevant data was subsequently eliminated. Additionally, flag columns were classified to facilitate more detailed feature analysis.

### Treating Outliers 
* Three numeric columns were identified to contain outliers through the application of the boxplot method. 
The distribution of the underlying features was extensively analyzed to confirm the presence of outliers. Based on this analysis, informed decisions were made regarding the
appropriate approach for handling these outliers.
* Rows with outliers which accounted for 0.5% of whole data were dropped from ‘AMT_TOTAL’ feature. Remaining features were skewed features with relevant clients data.
## Data Analysis

Univariate and Bivariate analysis was carried out to perform Exploratory Data Analysis (EDA).

`Countplot` and `pie chart` were used for understanding distribution of categorical variables with target variable.

For numerical variables following graphical presentatons were used:
* `distplot` to understand distribution of numerical variables across clients.
* `Boxplot` to understand distribution of numerical variables with respect to target variable.
* `Violinplot` to view spread of frequency and quantiles of underlying numerical varibles.
* `heatmap` to check the correlation of numerical variable with target variable.


## Insights and Conclusion

- 92% of clients are good applicants while 8% of clients are faulty applicants.
- In Gender, we have 7% of increased risk in Men.
- In Contract type, The Cash Loan seems to have 3% more risk of having defaulters.
- In Education, people with Secondary education as highest education has 9% increased risk.
- Single people seem to have 3% increased risk of being a defaulter.
- Laborers also seems to have 5% increased risk.
- Majority of the clients are actually of the age group 30-50.
- It is also noticed that the people with less age tend to represent more in TARGET 1 group.
- Similar to age(and highly correlated), clients with less experience tend to represent more in TARGET 1 group.
- If the Phone is changed within last couple of years there's an increased chance of being a TARGET 1 group client as 6% increased risk seen if phone changed less than a year.
- Previously refused loan seems to have 8% more increased risk.
- If the EXT_SOURCE_2 and and EXT_SOURCE_3 scores are lower, client tend to be riskier.
- Owning a home or property seem to reduce the risk by 1%,
- Majority of the client has salary between 100k and 250k Rupees.
- Most of the loan amounts are less than 800k Rupees, though we have outliers till 4M Rupees.
- Final credit amount on the last application is highly positively correlated with amount of credit asked by client on previous application.
- Loan amount and annuity amount are highly positively correlated also clients Income amount is also positively related to loan amount.
- Rating of Clients registered city is highly correlated with clients living region.
## Tech Stack

This data analytics project utilizes the following technologies and tools:

- Programming Languages: Python
- Data Analysis Libraries: Pandas, NumPy, Scipy
- Data Visualization: Matplotlib, Seaborn
- Other Tools: Jupyter Notebook, Git
