---
layout: post
title:  "Data Science Methods for Small Dataset (Regression)"
author: Pahul Preet Singh Kohli
categories: [Machine Learning, Regression, Small Dataset, Problems & Solutions, Data Science] 
image: assets/images/small-dataset.jpeg
description: "Small data sets are trickier to handle, require a different set of algorithms and a different set of skills."
comments: false
---

Small data sets are trickier to handle, require a different set of algorithms and a different set of skills.

## Problem of Small Dataset
    
1.  **Outliers**: Outlier handling can be ignored if they form a very small portion of the dataset whereas for small dataset even a few outliers become a large portion of dataset and therefore, consequentially alter the model.
    

  

2.  **Cross-Validation**: In the small dataset, one can't keep out many samples, even when one does, number of observation in test data may be too few to give meaningful results.
    

3.  **Overfitting**: is more likely to occur in the small dataset and cross-validation doesn't help much for examining overfitting.
    

4.  **Noise**: become an issue whether it is in the target variable or any of the feature used for modelling.
    

 

## Technique/Solutions for Handling of Small Dataset


    

  

1.  **Data Review**: Since outlier affects the small dataset predictive ability more, the dataset should be reviewed and cleaned to minimise the outlier impact.
    

  

2.  **Feature Selection**: If the data is truly limiting, explicit feature selection is essential. Wherever possible, use domain expertise to do feature selection or elimination, as using all feature is very likely to cause overfitting.
    

  

3.  **Simpler models**: Prefer simpler models and limit the number of parameters to be estimated for the model.
    

4.  **Ensemble approach**: Building a simpler model and then using the stacking approach for prediction. This approach tends to reduce overfitting without an increase in parameter to be estimated.
    

  

5.  **No cross-validation data**: If the number of observations is small, don't use cross-validation for hyperparameter optimization.
    

  

6.  **Regularization**: Regularization is way to produce more robust parameter estimates and is very useful in small data space. Lasso or L1 regularization produces fewer non-zero parameters and indirectly does feature selection. (example of regularizations: Lasso, Ridge, Elastic net)
    

  

7.  **Confidence intervals**: Try to predict with margin of error, rather than point estimates.
    

  

**Additional points**:

Rule of thumb for determining the minimum number of subjects required to conduct multiple regression analyses *[4]*:

-   N > 50 + 8m (where m is the number of independent variables) is needed for testing multiple correlation
    
-   N > 104 + m for testing individual predictors.
    
### References

1.  [https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89](https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89)
    
2.  [https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89](https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89)
    
3.  [https://www.edupristine.com/blog/managing-small-data](https://www.edupristine.com/blog/managing-small-data)
    
4.  [https://www.tandfonline.com/doi/abs/10.1207/s15327906mbr2603_7](https://www.tandfonline.com/doi/abs/10.1207/s15327906mbr2603_7)

