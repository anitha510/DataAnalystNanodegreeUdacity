# Diamonds Data Exploration

## Dataset
The data consists information about 113K loans with 81 features describing about the loan and the borrower.

The dataset can be found in https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv
with feature documentation available at https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1548287925106000

- Credit Rating for rows prior to 2009 are in Credit Grade column and post July 2009 are in 'Prosper Rating (Alpha)'. So, both columns were combined into one
- About 133 rows has an invalid Credit Score, so these we not considered during the plot
- Features having Nan values are ignored during the plot

## Summary of Findings

- Distribution of Lender Yield looks almost unimodal with an exception of a peak at the bin '0.30 - 0.31' and a bit left skewed
- For Credit Rating unexpectedly, significant percent of the loan is given to HR- High Risk borrowers. And also, the average yield for this credit rating is around 0.3, which explains the peak in the Yield histogram.
- By breaking down to Listing category, we could see that for Personal Loan and Student use the data is distributed bit more than other categories having less data. For Home improvement, we could see that comparatively it has less outliers in the bottom of the plot, suggesting higher yield with less risk for this category.
- Distribution of Investors is highly left skewed and also about 24% of the Investors count is 1. So, Log transformation is done for Investors with value more than 1 and the distribution is found to be unimodal with 2 as the center or close to 100 investors.
- Also, we could see that the trend when number of investors goes higher the Yield and Loss goes lower. And when Credit Rating/Prosper Score/Credit Score is low then the yield is high and vice versa.
- DebtToIncomeRatio and IsBorrowerHomeowner are not correlated to Yield/Loss.

## Key Insights for Presentation

I have started the presentation with the distribution of the targeted feature, Lender Yield and the plotted it against the main features Credit Score, Prosper Score and Credit rating to project the relationship between them and also done regression fitting to show the negative correlation. Then, plotted the same for each listing category to see the outliers more clearly.
Then, we looked at the time line for Average Return/Loss/Yield per month and average loans per month to see the trend.
