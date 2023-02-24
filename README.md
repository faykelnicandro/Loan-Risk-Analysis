# Loan Risk Analysis

## Outline
* Business Problem
* Data Understanding
* Data Cleaning and Feature Engineering
* Data Analysis
* Data Preparation
* Modeling
* Conclusion

### Business Problem

**Background**<br>

Money lending occurs in almost every business in the world. People with much money will lend it to those who need it. They do not lend their money for free; they charge interest. The larger amount and the longer term will result in a higher interest rate. This could occur in a bank, from company to company, or even from person to person.<br>

In reality, this lending process is not as simple as it appears. There are so many things to consider to make sure that the borrower can and will pay back the loaned money and the interest.<br>

**Problem Statement**<br>

A lending company client wants to lend their money to borrowers in a riskless condition for the company. As a Data Scientist, they want us to predict which customer is in the good category based on their credit risk to get the loaned money.<br>

**Goals**<br>

As the problem given, this analysis' goal are to be able to predict which customer are Good Borrower and which are Bad Borrower. Good Borrower is someone who repays all the loaned money on time, and the Bad Borrower is someone who repays a loan late or does not repay it at all.<br>

By knowing this, the company can avoid borrower with higher risk (late repay or not repay).<br>

**Analytical Approach**<br>

Classification Machine learning will be used to determine which borrowers are less risky and more likely to repay the loan by using ROC/AUC performance.<br>

### Conclusion<br>

The LightGBM model after hyperparameter tuning is the best model, with a ROC AUC performance of `0.971128`. This means this model can correctly classify more than 97% of the data.<br>
The parameters used are:
1. learning_rate: 0.1 
2. max_bin: 275
3. min_data_in_leaf: 30
4. num_iterations: 150
5. num_leaves: 41<br>

Beside that, there are a few things that could be used to perform `early steps to identify bad borrowers,` including the following:
1. Educational and small business purposes need more attention and further action when applying for the loaned money.
2. Further action, borrower analysis, and supervision are recommended for 60-months installment.
3. Further action, borrower analysis, and supervision are recommended for borrowers from Nebraska, Iowa, Idaho, Mississippi, and Tennessee.
4. Further action, borrower analysis, and supervision are recommended for 'other' category in home ownership are recommended when applying for the loaned money.
5. The lower the grade, the more action and borrower analysis are required.
