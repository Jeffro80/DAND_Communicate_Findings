# Loan Data from Prosper Exploration
## by Jeff Mitchell


## Dataset

The dataset used was loan data from Prosper. This contained nearly 114,000 loans from first quarter 2006 to the fourth quarter 2013. The data was obtained from [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv). 


## Summary of Findings

The overall completion rate of loans from the filtered data was 70%. Most of the members were employed full time. Home ownership appeared to have little impact on loan completion and the proportion of members owning their home was also close so these results were not due to a skew in the number of people owning their home. The largest listing category was Debt consolidation followed by Not available. Debt consolidation did not appear to have an impact on Loan completion rates, when compared to all other listing categories combined, however we did see some differences between categories. Vehicle and Engagement Ring loans had the highest levels of loan completion while Green Loans and Personal Loans had the lowest levels of completion.

The original loan amounts were skewed to the right and tended to cluster around $5000 intervals. A log transofrmation on the loan amounts showed the distribution to be normal. Monthly loan payments were also right skewed and showed that most payments were under $500 with the average being around $200. Loan payments between $750 and $1000 had the lowest completion rate and those above $1500 had the highest completion rates. These monthly loan payment amounts were outside of the amounts paid by most members (below $500) so can be seen as outliers. Within the range of Monthly Loan Payments made by most members (< $500) there was not a lot of difference in loan completion rates.

Debt-to-income rates had a right skew with most values being below 0.5. Loan completion rates lowered as the Debt-to-income ratio increased, however, this effect was not pronounced until above 0.3 which was higher than the ratio for most of the members. This suggests that these higher ratio values are subject to greater variance. Other financial indicators were as expected, with loan completion increased for members with higher average credit scores and lower average Borrower APR. Average Stated Monhtly Income was also higher for members that completed their loans.

Short-term (12-month) loan terms were much more likely to be completed, with 60-month terms the least likely. The vast majority of loans were for a 36-month period. Increasing loan period tended to reduce the likelihood of a loan being completed.

I started my univariate exploration by looking at the overall loan completion status and then looking at the counts for a number of the variables to understand how the data was distributed. Where necessary I grouped categories and dropped data that was missing to provide a better picture of the data. I then moved to looking at the proportions by category for categorical data. Some of the data such as Monthly Loan Payments and Stated Monthly Income required log transformations. I used a variety of graphs such as countplots, histograms and boxplots to develop a picture of the variables within the data.

I had to remove some outliers from the data that were skewing the results as well as remove data that was missing. Examples included annual income figures of $1 that looked like they may have been place holders. There were also credit scores bwtween 0 ad 19 that looked incorrect and some high Stated Monthly Income values that I removed.

For the bivariate exploration I started by looking at pairwise correlations between numeric and categorical variables. These did not show any that were unexpected. I focused my exploration on the effect of various variables on Loan Completion. To do this I plotted the proportion of Completed and Not completed loans by each level of categorical variables to look for trends. Many of the trends that I noticed appeared to be impacted by outliers or due to smaller sample sizes in the categorical levels that moved away from the mean.

I had to perform some cleaning on the data in order to get the plots to work. For instance, the filtered data resulted in there being no data from Q4 2005 and Q1 2006 which caused errors. I had to remove these categories to get the plots to work. I also had to create columns to hold the bins for some variables so that I could plot them correctly.

 

 


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.