# deep-learning-challenge

## Overview
 The purpose of this this analysis is to train a model to determine the whether or not an applicant will be successful if they are funded by this foundation.

 ## Data Preprocessing
* The variable target for this model was "IS_SUCCESSFUL" in this case a 0 means yes and a 1 means no.

* For the variable features we used the columns listed below.![the columns listed below](/Images/variable_features.png)

    We only dropped 2 columns from the original data frame. The EINE and NAME columns, any other columns dropped seemed to provide little if any benafit to the models accuracy predictions.

## Compiling, Training, and Evaluating the Model
* Many diffrent model layouts were tried and I settled on using a Linear activation for the inputs, Relu activation for the 2nd and 3rd hidden layers, and a Sigmoid activation for the output layer.
This image shows what the model looks like. ![Alt text](/Images/nural_model.png).

* Unfortunatly I was unable to reach the minimum threshold of 75% accuracy. The max i was able to get was 73.88%
![](/Images/max_accuracy.png)

* Many diffrent changes were attempted and I was never able to reach even 74%. 

    * I tried dropping diffrent features such as "STATUS" and "USE_CASE" and "ASK_AMT" all of which had a negative or minute impact of the models predictive out comes
    
    * I adjusted the bin size by both increasing and decreasing the amount of outliers that exsist in the columns "CLASSIFICATION and "APPLICATION_TYPE".
    
    * I Played with the number of Nurons and hidden layers as well as with the activation types of those layers. I also fiddled with the number of epochs. 200 seemed to get me the most consistant results.

