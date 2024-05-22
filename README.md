# Deep Learning

## Overview of Analysis
The purpose of this analysis is to help the nonprofit foundation Alphabet Soup create a machine learning and neural network model that will accurately predict whether applicants will be successful if funded by Alphabet Soup.  The dataset included more than 34,000 organizations that have received funding from them over the years.  

## Results
* Data Preprocessing
    * The target column was the "IS_SUCCESSFUL" column in the dataset to determine whether the funding was used effectively and successfully.
    * The features of the model can include name, application type, affliation, classification, use case, organization, status, income amount, special considerations, and amount asked. These features can be changed to optimize the predictive accuracy of the model.  Not all features needed to be included or used.  However, in order to optimize the model, I used all the features listed above.
    * The features that were removed from the input data was EIN and possibly names which were both idenfitication columns.  For the first model, both EIN and names were removed from the model.  However, in order to optimize the model for a predictive accuracy above 75% I added back the name column to get it above 75%. 

* Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
