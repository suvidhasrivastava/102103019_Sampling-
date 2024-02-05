### Introduction
Challenge of handling imbalanced datasets. It employs five distinct sampling methods to create samples, evaluating the performance of five machine learning algorithms on each.
### Dataset 
The dataset exhibits an imbalance, visually represented in the following graph:

### Addressing the Imbalanced Dataset
 
To counter the imbalance, we employed Random Over-Sampling using the imblearn library. This method generates new samples for minority classes through random sampling with replacement.

### Determining Sampling Size

The formula used = $$n = \frac{Z^2 * p * (1-p)}{E^2}$$
Here Z is Z score corresponding to the desired confidence level, p is the estimated proportion with certain characteristic and E is the desired margin of error.
 For this study, Z=1.96 (95% confidence), p=0.5, and E=0.05, resulting in n=384.
 
### Sampling Methods used 
Simple Random Sampling: Each member of the population has an equal chance of selection.(Sample1)

Simple Stratified Sampling: The population is divided into homogeneous subpopulations (strata) based on specific characteristics, with each stratum sampled using simple random sampling.(Sample2)

Systematic Sampling: Members are selected at regular intervals, in this case, every 3rd person.(Sample3)

BootStrap Sampling: A method involving repeated drawing of sample data with replacement to estimate population parameters.(Sample4)

Cross Validation: This involves dividing the data into folds, using one fold as validation, and training the model on the remaining folds. This process is repeated, and results are averaged for a robust estimate of model performance.(Sample5)


### Algorithms used 
 Random Forest, XGBoost, KNN, SVM, Logistic Regression

## Results
Output Table 
| Model               | Sample1 | Sample2 | Sample3 | Sample4 | Sample5 |
|---------------------|---------|---------|---------|---------|---------|
| RandomForest        | 0.9914  | 0.9914  | 0.9935  | 0.9828  | 0.9883  |
| XGBoost             | 0.9569  | 0.9828  | 0.9804  | 0.9828  | 0.9844  |
| KNN                 | 0.9483  | 0.8793  | 0.9477  | 0.9828  | 0.9883  |
| SVM                 | 0.6897  | 0.7155  | 0.7124  | 0.9828  | 0.9883  |
| LogisticRegression  | 0.8621  | 0.9310  | 0.8824  | 0.9828  | 0.9819  |

## Final Result
Best Model -> Random forest  
Accuracy -> 0.9914(Highest)

