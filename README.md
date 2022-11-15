# Prosper Loan Data Exploration
## by Yusuff O. Olaniyi


## Dataset

> Original dataset contains approximately 114,000 loans with 81 variables on each loan, including loan amount, borrower rate, current loan status, borrower income, borrower's employment status and many others.

> Since our main goal here is EDA , I merged assessing and cleaning steps into one to make it concise.


## Data Assessing and Cleaning
> 1. choose subset of features important
> 2. drop rows with null value in the colunms BorrowerAPR and CreditScoreUpper
> 3. drop duplicated rows
> 4. fill missing values in the Occupation, BorrowerState and DebtToIncomeRatio
> 5. replace Full-time in EmploymentStatus with Employed and fill missing values
> 6. Split LoanOriginationQuarter column into Quarter and Year and extract Month from ListCreationDate
> 7. create ListingCategory column and assign actual value to the numerical values 'ListingCategory (numeric)'
> 8. drop all rows with credit score less than 300,create CreditScore column and assign grades to the numerical values in CreditScoreRangeUpper
> 9. convert EmploymentStatus, Year, Quarter, Month and CreditScore into ordered categorical types
> 10. drop rows with MonthlyLoanPayment greater than 1500



## Summary of Findings

> I am interested in deteriming which factor(s) contribute to making a good FICO (Credit) score which might in turn determines the assessibilty and amount of loan from ProsperLoan. Also, I will also like to check for what category of people take most loans.

>  The loan amount ranges from 1,000 to 35,000 with 4,000 being the most popular followed by 15,000 and 10,000. More than 6,000 people also borrowed 2,000, 4,000 and 5,000.

> The distribution of MonthlyLoanPayment is multimodal with the highest peak at 200, a smaller one at 150 and another one at 350.

>The distribution of StatedMonthlyIncome is unimodal and right skewed with most values between 0 and 2000, the peak is 4,000. Monthly income above 30,000 were considered as outliers, and so, needed to be dropped

> The distribution of DebtToIncomeRatio is unimodal with peak around 0.2. Most values are between 0 and 1 and right skewed with an unusual peak at 0.25. Showing that 10% of the borrowers has a debt-to-income ratio of 0.25 

> The distribution of APR looks multimodal. A small peak centered at 0.1, a large peak centered at 0.2. There is also a small peak centered 0.3. Additionally, there is a very shape peak between 0.35 and 0.36. Only very few loans have APR greater than 0.4.

> Califonia takes the lead in BorrowerState, followed by Florida, New York and Texas. While Maine and Wyoming has the least number

> 50% of the borrower have a good credit score, 70% are employed or have a full-time job and 50% of the loans are for debt consolidation

> Loan amount seem to be independent of depend on the debt-to-income ratio, but has a positive correlation with monthly income, as expected. It also has a high positive correlation with Monthly loan payment. APR and Borrower rate have a correlation of 0.99, and they both have a negative correlation with loan amount.

> The higher the loan amount the longer the term of payment. Loan amount, also, increases with better credit score. Self-employed and employed borrowers have access to higher loan amount part-time, retired and unemployed borrowers have access to more of lesser amount of loan.

>Borrowers with better credit score have higher Stated monthly income as well as Monthly loan payment. Borrower APR and Rate also drop with better credit score. More of employed borrowers have a minimum of good credit score. Borrowers with minimum of good credit score have more home owners than non-home owners

> Borrowers with higher credit score seem to earn more and pay more loans per month.

> APR drops as the credit score improves for all employment statuses. 'Not employed' borrowers has the highest APR except for those with Poor credit score. Retired Borrowers with Poor credit score have the highest APR
> StatedMonthlyIncome increases with better credit score across all employment status, although, it seems not to follow for 'Not employed' as the pattern fluctuates. Also, it seems most borrowers who have decided not to share their employment status earn well.

> The higher the APR, the lower the loan amount and vice versa. This only changes when the borrower has a credit score of 800 and above.

> All employment status shows a positive slope between Loan amount and Monthly income except Unemployed which maintained a slightly negative relationship. Employed and Other have a very strong positive relationship.


## Key Insights for Presentation


> January has the highest number of loans listed as expected from starting of new year, whereas april sees the least number of loans listed. Despite this, the fourth quarter recorded the highest number of laons. There is an upward trend in loans listed with each passing year from 2009 to 2013 while there is a reduction in the number of loans in 2014.

> The distribution of APR looks multimodal. A small peak centered at 0.1, a large peak centered at 0.2. There is also a small peak centered 0.3. Additionally, there is a very shape peak between 0.35 and 0.36. Only very few loans have APR greater than 0.43.

> Distribution of DebtToIncomeRatio is unimodal peak around 0.2 with unusual peak around 0.25 which indicates most people prefer 1:4 ratio of debt to Income which is a good thing.

> As the loan amount increases, the range of APR decreases. Meaning that, the borrower APR decreases with increase of loan amount.

> The borrower APR decreases with the increasingly better score. Borrowers with the best Credit Score have the lowest APR. It means that the Credit Score has a strong effect on borrower APR.

> Borrowers with Poor credit score have most loans below 5000 and the distribution grows taller as the cedit score improves. Hence, as the credit score gets better, the loan amount also improves.

> The higher the APR the lower the loan amount and vise versa, except for people with credit score of 800 and above where the loan amount increases with the APR.

> On the average, debt-to-income ratio rises between Poor credit score and Good and then drops between Good and Excellent

> It seems loan amount is more dependent on credit score than employment status as unemployed borrowers with excellent credit score have an average loan of 8000. 

> Unemployed borrowers earn the least monthly income, as the monthly income increase with better credit score for all employment status. Also, except for borrowers whose employment status is 'Not available, loan amount also increases with better credit score.

