In this project, we will walk through the full data science life cycle, from
data cleaning and feature selection to machine learning. We will focus on
credit modelling, a well known data science problem that focuses on modeling a
borrower's [credit risk](https://en.wikipedia.org/wiki/Credit_risk). Credit has played a key role in the economy for centuries
and some form of credit has existed since the beginning of commerce.
We'll be working with financial lending data from [Lending Club](https://www.lendingclub.com/). Lending Club is
a marketplace for personal loans that matches borrowers who are seeking a loan
with investors looking to lend money and make a return.
You can read more about their marketplace [here](https://www.lendingclub.com/public/how-peer-lending-works.action).

Each borrower fills out a comprehensive application, providing their past
financial history, the reason for the loan, and more. Lending Club evaluates
each borrower's credit score using past historical data (and their own data
science process!) and assign an interest rate to the borrower. The interest
rate is the percent in addition to the requested loan amount the borrower
has to pay back. You can read more about the interest rate that Lending Club
assigns [here](https://www.lendingclub.com/public/borrower-rates-and-fees.action). Lending Club also tries to verify each piece of information
the borrower provides but it can't always verify all of the information
(usually for regulation reasons).

A higher interest rate means that the borrower is riskier and more unlikely to
pay back the loan while a lower interest rate means that the borrower has a good
credit history is more likely to pay back the loan. The interest rates range from
5.32% all the way to 30.99% and each borrower is given a grade according to the
interest rate they were assigned. If the borrower accepts the interest rate,
then the loan is listed on the Lending Club marketplace.

Investors are primarily interested in receiveing a return on their investments.
Approved loans are listed on the Lending Club website, where qualified investors
can browse recently approved loans, the borrower's credit score, the purpose for
the loan, and other information from the application. Once they're ready to back
a loan, they select the amount of money they want to fund. Once a loan's requested
amount is fully funded, the borrower receives the money they requested minus the
[origination fee](https://help.lendingclub.com/hc/en-us/articles/214501397) that Lending Club charges.

The borrower then makes monthly payments back to Lending Club either over 36
months or over 60 months. Lending Club redistributes these payments to the investors.
This means that investors don't have to wait until the full amount is paid off
to start to see money back. If a loan is fully paid off on time, the investors
make a return which corresponds to the interest rate the borrower had to pay in
addition the requested amount. Many loans aren't completely paid off on time,
however, and some borrowers [default](https://www.lendingclub.com/public/collections-process.action) on the loan.

While Lending Club has to be extremely savvy and rigorous with their credit
modelling, investors on Lending Club need to be equally as savvy about determining
which loans are more likely to be paid off. While at first, you may wonder why
investors would put money into anything but low interest loans. The incentive
investors have to back higher interest loans is, well, the higher interest! If
investors believe the borrower can pay back the loan, even if he or she has a
weak financial history, then investors can make more money through the larger
additional amount the borrower has to pay.

Most investors use a portfolio strategy to invest small amounts in many loans,
with healthy mixes of low, medium, and interest loans. In this project, we'll
focus on the mindset of a conservative investor who only wants to invest in the
loans that have a good chance of being paid off on time. To do that, we'll need
to first understand the features in the dataset and then experiment with building
machine learning models that reliably predict if a loan will be paid off or not.
