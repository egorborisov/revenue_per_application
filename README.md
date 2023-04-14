# Reimagining Credit Scoring Evaluation: "Revenue per Application"
If you have a credit scoring model that requires improvement, the typical problem statement is usually phrased as either "Reduce delinquency without decreasing approval rate". The problem statement simplifies the evaluation process significantly as we only need to measure changes in one metric, assuming that all others are constant. Ans also achieving the same approval level is feasible, as we can accurately calculate it with 100% precision through a retrospective test. 

So it is common to observe such pictures at credit scoring conferences or during vendor presentations:

<img src="https://cdn-images-1.medium.com/max/1600/1*Lk6NlNIlmxysK4EncXCPig.png"/>

When analyzing delinquency, it's important to consider potential hidden factors. For example, a new model might have a lower delinquency rate in terms of the number of loans, but a higher average loan amount in delinquency. To get a complete picture, it may be necessary to analyze this aspect separately or calculate a weighted delinquency rate. 

Both business metrics and delinquency depend on the loan amount distribution. To ensure the validity of the approach, it's essential to verify that it remains constant too, especially when using risk-based limit strategies

<img src="https://cdn-images-1.medium.com/max/1600/1*gSrfoqyhr0fV8XuLJzgXPg.png"/>

It's possible that not all loans that are approved will be disbursed since a client has the option to decline the loan even after approval. Therefore, it's important to consider the disbursement rate, which is the ratio of approved loans that are actually disbursed. This rate can also be affected by the scoring model used.

<img src="https://cdn-images-1.medium.com/max/1600/1*Zrb9B0SYPd9Xu22PKCZTYQ.png"/>

In this case, the approach of fixing all indicators at the previous level and measuring only the change in delinquency is suitable. However, what if we want to test several changes at once or more complex changes, such as the limit policy? Or, what if we want to compare scoring and underwriters? Also, keep in mind that if risk-based pricing is being used, the comparison based on the presented scheme may not be accurate.

### Revenue per Application

The main objective of a credit scoring system is to increase a loan originator's revenue. We can use the profitability metric by deducting the money issued to the customer from the funds received from them while disregarding other expenses. To compare segments of different sizes, we need to normalize this metric based on the number of applications in each segment. It's crucial to use the number of applications, not approvals or disbursements, to ensure accurate results when approval rates vary. Consequently, we get a metric called "revenue per application":

<img src="https://cdn-images-1.medium.com/max/1600/1*Z6sZy8OPKZaxJt5ZaRnUQQ.png"/>

Let's confirm that this metric includes all the previously mentioned metrics. For instance, if the approval level increases while all other variables remain constant, the numerator in the formula will increase, and therefore, the revenue per application will also increase.

<img src="https://cdn-images-1.medium.com/max/1600/1*Qi-PnBAF6LeOUlASI1ci5A.png"/>

_Examining new paid sources of customer data can also benefit from this metric. For instance, a mobile operator is ready to provide us with an API that includes specific customer information for a fee of x dollars. By comparing this cost with the variation in revenue from the application, we can make an informed choice._
