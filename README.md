# Challenge_17

## Overview of the analysis

Using the credit card dataset from the Lending Club, we want to get the best possible model to classify new applications as low or high risk based on their specific characteristics.

Notice that, since low-risk requests are a small portion of the total requests, this is, by definition, an unbalanced basis, thus, we'll need to apply some techniques to rebalance the basis to enhance the model's accuracy. 

Finally, to identify the best model among the different options, we'll use the Balanced Accuracy Score, the Precision and Recall Scores.

## Results

To accomplish our duty, we created 6 different models with different results shown below: 

### Undersampling

![Undersampling](Undersampling.png)

### Oversampling

#### Naive Random

![Naive](Naive.png)

### SMOTE Oversampling

![SMOTE](SMOTE.png)

### Combination 

![Combination](Combination.png)

### Ensemble

![Ensemble](Ensemble.png)

### Adaboost

![Adaboost](Adaboost.png)

# Summary:

Recall: 

- Precision measures the accuracy of positive predictions (TP/(TP + FP)).
- Recall is the accuracy to correctly find all the positive predictions (TP / (TP +FN))
- Specificity is similar to Recall but for negative values (TN / (TN+FP))

F1 Score & Geo Mean are non aritmethic means designed to jointly measure some of the metrics described before.  

Due to the nature of the project: much higher low risk than high risk, I believe our focus must be the correct prediction of negative values, thus, we may want to focus on Specifity measure and Geometric Mean. 

As expected, Adaboost truly enhances the predictions of the models as shown in the different metrics reaching the highest results among all the projects. 

In a future step, we may want to create more specific categories, for example, split the low-risk profiles vs the amount requested, makes sense to belive that a low-risk profile may vary its riskiness based on the amount requested.  
