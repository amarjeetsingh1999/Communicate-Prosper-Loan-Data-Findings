# Prosper Loan Data Exploration
## <i>by Amarjeet Singh</i>


## Dataset

In this exploration, i used the [Prosper Loan data set](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv) which contains 113,937 listings with 81 variables on each listing with data available for listings from late 2005 till early 2014. There were 21 types of listing categories available with term length option of 12-month, 36-month or 60-month. Also there's data available about the borrower and certain scores which indicate the credibility of the borrower.

This [data dictionary](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0) explains the variables in the data set.

[Prosper Marketplace, Inc.](https://www.prosper.com/) is a San Francisco, California-based company in the peer-to-peer lending industry. Prosper Funding LLC, one of its subsidiaries, operates Prosper.com, a website where individuals can either invest in personal loans or request to borrow money. Prosper Marketplace is America's first peer-to-peer lending marketplace, with over $7 billion in funded loans. Borrowers request personal loans on Prosper and investors (individual or institutional) can fund anywhere from $2,000 to $35,000 per loan request. Investors can consider borrowers’ credit scores, ratings, and histories and the category of the loan. Prosper handles the servicing of the loan and collects and distributes borrower payments and interest back to the loan investors.

Prosper verifies borrowers' identities and select personal data before funding loans and manages all stages of loan servicing. Prosper's unsecured personal loans are fully amortized over a period of three or five years, with no pre-payment penalties. Prosper generates revenue by collecting a one-time fee on funded loans from borrowers and assessing an annual loan servicing fee to investors.


## Summary of Findings

The following insights were found during exploration:
1. There was a big dip in the number of listings from Q4 2008 into 2009-10. It took almost four years for listing levels to reach the Q2 2008 levels.
2. Most of the borrowers were assigned a prosper rating of C at the time the listing was created.
3. It was observed that most of the loans were for Debt Consolidation purpose.
4. Interest rates are relatively high with an average of 19.28%. As most of the listings were for debt consolidation, these high interest rates might still be better than the interest rates the borrowers would have to pay for old debts.
5. Most of the borrowers were employed and earn less than $75,000 per year which can be an explanation to why most of the loans were for debt consolidation purposes.
6. A significant number of borrowers were on their second or third loan with Prosper at the time of listing.
7. Majority of loans were of term lenght of 36 months.
8. Starting from Q1 2006, the number of non-perfroming loans went from 85 and rose to a peak of 1,477 in Q2 2008, before dropping until Q1 2009 when Prosper had no listings.
9. Non-performing loans consistently have lower(high risk) prosper scores than performing ones at each level of total prosper loans.
10. The visualization shows that higher the credit score, the more likely the loan is to perform.
11. A risky Prosper rating does correlate to a higher rate of non-performing loans, and less risky ratings show fewer non-performing loans.
12. Unemployed borrowers' income range is having a very long range of spread for debt to income ratio.
13. Borrowers' with income range of $100,000+ take huge amounts of loans as compared to borrowers' falling into other income ranges.
14. As expected, the estimated loss is highest for borrowers' with $0 income and those who are unemployed.
15. Borrowers with loans of term length 60 months seem to be more credit worthy on average.
16. The shorter 12-month terms appear to perform better than their 36-month and 60-month counterparts, at least in the limited data sample that we have.
17. It's observed that lower-risk(high Prosper score) loans don’t always outperform their higher-risk counterparts.
18. If the estimated loss and debt to income ration are low, the prosper score lies on the lowest risk side and this effect is even more pronounced for loans of term length 36 months.
19. Prosper Score is better i.e, on low risk side for low DebtToIncome ratio given Estimted Return is higher and this is even more pronounced for loans of term length 12 months.
20. Prosper Score is high for low debt to income ratio given that borrower has no prior loans or less no. of loans undertaken at listing time and if taken they be of term length 36 months for this observation to be more pronounced.


## Key Insights for Presentation

1. The listings with low(high risk) Prosper Scores, on average under 6 in this case, consistently fall under the non-performing category eventually no matter how many listings there are already with the borrower at the time that particular listing was created.
2. Prosper’s risk rating system is fairly predictive in identifying the group of loans that has a higher chance to eventually default. Indeed, over 8% of “high-risk” HR loans and around 10% of D loans have failed to perform, while less than 3% of “low-risk” AA loans have defaulted (or been charged off). The risk ratings in between decline in an almost linear fashion going down the scale of riskiness with an exception of loans with Prosper rating of D. However, looking at the loans on a quarterly basis showed that the Prosper Rating is not necessarily as predictive at smaller sample sizes. There are many(a lot) quarters in which E-, D-, or sometimes even B-rated loans ended up with higher non-performance rates than HR loans. The data is chunkier from quarter to quarter, as opposed to over the whole sample size.
3. In this visualization dark colored dots are visible which denotes higher(low risk) Prosper Score.
If the debt to income ratio are low, the prosper score lies on the lowest risk side given that estimated loss is low or estimated return is high. As the estimated loss becomes high, the prosper score tends to shift towards high risk side irrespective of the debt to income ratio.
Overall it could be concluded that for borrowers with low debt to income ratio if the Prosper score is high(low risk), then the estimated loss is low and estimated return is low too. Also it can be seen that borrowers with low debt to income ratio tend to take more loans but also have high Prosper scores and make on time payments as compared to their counterparts with high debt to income ratio.

## View the Presentation

1. Clone this repository.
2. `cd` into the cloned repository and run the below command from the terminal or command line
> `jupyter nbconvert <file_name>.ipynb --to slides --post serve --template output_toggle`
This should open a tab in your web browser where you can scroll through your
presentation. Sub-slides can be accessed by pressing 'down' when viewing its parent
slide.