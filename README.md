# Reimagining Credit Scoring Evaluation: "Revenue per Application"
If you have a credit scoring model that requires improvement, the typical problem statement is usually phrased as either "Reduce delinquency without decreasing approval rate". The problem statement simplifies the evaluation process significantly as we only need to measure changes in one metric, assuming that all others are constant. Ans also achieving the same approval level is feasible, as we can accurately calculate it with 100% precision through a retrospective test. 

So it is common to observe such pictures at credit scoring conferences or during vendor presentations:

<img src="https://cdn-images-1.medium.com/max/1600/1*Lk6NlNIlmxysK4EncXCPig.png"/>

When analyzing delinquency, it's important to consider potential hidden factors. For example, a new model might have a lower delinquency rate in terms of the number of loans, but a higher average loan amount in delinquency. To get a complete picture, it may be necessary to analyze this aspect separately or calculate a weighted delinquency rate.
Both business metrics and delinquency depend on the loan amount distribution. To ensure the validity of the approach, it's essential to verify that it remains constant too, especially when using risk-based limit strategies
