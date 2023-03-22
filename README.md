# Prosper Loan Data: Exploratory and Explanatory data visualization

## Oyedele Samuel


## Dataset

> This is the dataset about loans record with various loan variables. This dataset contains 113,937 loans with 81 variables including loan amount, current loan status, term, prosper score, borrower rate (or interest rate),borrower income, and many others. 

> A subset dataset of 77,543 loans with 20 variables was used after data wrangling.
Some of the variables are: `Term`, `LoanStatus`, `BorrowerRate`, `ProsperScore`, `IncomeRange`, `IsBorrowerHomeowner`, `DebtToIncomeRatio`, 'StatedMonthlyIncome', `LoanOriginalAmount`, `MonthlyLoanPayment`.

> The dataset can be found in the <a href = "https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv."> here </a> (https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv)


> Here is the link to the <a href = "https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0"> data dictionary </a>

## Data Wrangling

> In this section, the dataset was gathered, accessed it to inspect any issues or outliers in the data and clean the data for better exploratory visualization.

### Assessments - Issues

- Missing values in `BorrowerRate`, `ProsperRating (Alpha)`, `ProsperScore`, `Occupation`, `EmploymentStatus`, `EmploymentStatusDuration`, `DebtToIncomeRatio`
- Replace value (True - Homeowner, False - No Homeowner) in `IsBorrowerHomeowner`
- Replace the values of `ListingCategory (numeric)`
- Convert `StatedMonthlyIncome` to nearest whole number
- Extract columns (month, year) from `LoanOriginalDate`
- Convert the data types of `EmploymentStatus`, `ProsperScore`, `ListingCategory (numeric)`, `IsBorrowerHomeowner`
- Rename some unclean variables
- Convert `LoanStatus`, `ProsperScore`, `ProsperScore (Alpha)`, `Loan Original Month`, `Year`, `Income Range` into ordered categorical type

## Summary of Findings

After data wrangling and exploratory visualization:

- The loan original amount distribution is trimodal, with one peak at 5000, second peak at 10000, and third peak at 15000.

- In Employment Status: Employed people tend to get the most loans compared to other categories.

- More loans are given in 36 term (3years). Over 60% of loans given to borrower are home owner. most of the loans are still on current status. 2013 is the year with the most frequency of loans.

- Most loans are collected based on debt consolidation which was more than other listing category. This implies that most borrowers collect loans to pay up their debts.

- I found that was a strong relationship between the loan original amount and income range, higher the income range the higher the loan amount given.

- There was a strong postive correlation between loan original amount and monthly loan payment.

- There was a weak postive correlation between loan orginal amount and stated monthly income but borrowers with high monthly income tend to get high loans.

- I found that they was some postive relationship between the categorical variables (income range, prosper score, loan orgination year, is borrower home owner and the numerical variables (loan original amount and monthly loan payment). The average loan original amounts and monthly loan payment increased yearly. Highest income range tend to have the highest average loan orginal amount and monthly loan payment.

- High loan amounts are issued out when there's low debt income ratio (< 0.36). The lower the debt to income ratio, the higher the loan original amount.

- There was increased in average monthly loan payment across all income range.

- There was increased in loan original amount and monthly loan payment across the terms.

## Key Insights for Presentation:

> For the presentation, I focus my investigation some categorical features on loan original amount and monthly loan payment. I started by introducing some of the univariate explorations; loan original amount variable, income range, debt to income ratio, is borrower home owner then the pattern of monthly loan payment. 

> Scatter plots showing the relationship between the loan original amount and income range (a categorical variable), relationship between the loan original amount and monthly loan payment were plotted. I also check the relationship between loan original amount and loan status (categorical variable), monthly loan payment and stated monthly income.

> Afterwards, I investigate some of other categorical variables. Firstly, I use the box plots of loan original amount and monthly loan payment across year. I'm looking at how the loans are given out and paid across year. Two categorical variables, prosper score and loan origination year are investigated on loan amounts using strip plot based on selected debt to income ratio.

## Skills and Technologies used

- Python
- Pandas
- Matplotlib
- Seaborn
- Numpy
- Data Wrangling
- Data Visualization
