---
layout: post
title:  "Deployment Framework - Static Machine Learning Model"
author: Pahul Preet Singh Kohli
categories: [Machine Learning, Deployment, Data Science] 
image: assets/images/static_model_framework.png
description: "Static model is trained offline. That is, we train the model exactly once and then use that trained model for a while."
comments: false
---


**-   Separate Training from the Server:**
-   Static model is trained offline. That is, we train the model exactly once and then use that trained model for a while.
    

  

-   The model training is done on the local machine and once the model is complete, it is saved and transferred to server to make live predictions.
    

  

-   Packaging ML Model: the machine learning model is packaged as file in the following format (python):
    

	-   Pickle file: converts python object to byte stream.
	    
	-   Predictive model markup language: xml based file format for saving prediction model.
	    
	-   Joblib File: A faster method for saving the model trained on a large dataset.
	    
	-   Gzip File: compress model to save storage space
	    

  

-   The packaged ML model can be easily loaded by the server.
    

**-   ML Model as Standalone Model:**
    

-   Every pre-processing step and feature engineering is replicated on the server-side for transforming raw input.
    

  

-   The server loads the ML model only.
    

  

-   The transformed input is put in the model and the model outputs prediction in the required format.
    

  
  

**-   Advantage of static model:**
    

-   Static Model is cheaper to create and maintain than Dynamic Model which uses online training methodology.
    

  

**-   Drawback of static model:**
    

-   Many information sources through which data is extracted and trained on, change over time, therefore, the input data must be monitored.
    

  

### References

-   [https://medium.com/analytics-and-data/overview-of-the-different-approaches-to-putting-machinelearning-ml-models-in-production-c699b34abf86](https://medium.com/analytics-and-data/overview-of-the-different-approaches-to-putting-machinelearning-ml-models-in-production-c699b34abf86)
    
-   [https://developers.google.com/machine-learning/crash-course/static-vs-dynamic-training/video-lecture](https://developers.google.com/machine-learning/crash-course/static-vs-dynamic-training/video-lecture)
    
-   [https://www.kdnuggets.com/2017/09/putting-machine-learning-production.html](https://www.kdnuggets.com/2017/09/putting-machine-learning-production.html)
    
-   [https://cloudxlab.com/blog/deploying-machine-learning-model-in-production/](https://cloudxlab.com/blog/deploying-machine-learning-model-in-production/)
    
-   [https://christophergs.github.io/machine%20learning/2019/03/17/how-to-deploy-machine-learning-models/#tools](https://christophergs.github.io/machine%20learning/2019/03/17/how-to-deploy-machine-learning-models/#tools)

