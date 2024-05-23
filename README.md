# Deep Learning

## Overview of Analysis
The purpose of this analysis is to help the nonprofit foundation Alphabet Soup create a machine learning and neural network model that will accurately predict whether applicants will be successful if funded by Alphabet Soup.  The dataset included more than 34,000 organizations that have received funding from them over the years.  

## Results
* **Data Preprocessing**
    * The target column was the "IS_SUCCESSFUL" column in the dataset to determine whether the funding was used effectively and successfully.
    * The features of the model can include NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. These features can be changed to optimize the predictive accuracy of the model.  Not all features needed to be included or used.  However, in order to optimize the model, I used all the features listed above.
    * The features that were removed from the input data was EIN and possibly names which were both idenfitication columns.  For the first model, both EIN and names were removed from the model.  However, in order to optimize the model for a predictive accuracy above 75% I added back the name column to get it above 75%. 

* **Compiling, Training, and Evaluating the Model - Model 1 (non-optimized)**
     * Model 1 removed NAME and EIN columns from the training and testing data.
     * For the first model, there were 2 hidden layers with ReLu activation functions.  There were 43 neurons in the input layer and 1 neuron in the output layer.  The first hidden layer had 80 neurons, and the second hidden layer had 30 neurons.  
![Screenshot 2024-05-22 163529](https://github.com/imzxtingi/deep-learning-challenge/assets/150073701/c07b498d-b88b-419b-a842-07d4234956be)
   * This model had an accuracy predictor of 72% and with 56% loss.  This particular model is not very good at predicting successful funding. 
![Screenshot 2024-05-22 163551](https://github.com/imzxtingi/deep-learning-challenge/assets/150073701/4f51f3d5-3352-4f84-9bf5-5164e4fe11f9)

* **Compiling, Training, and Evaluating the Model - Model 2 (optimized)**
     * Model 2 removed EIN column from the training and testing data.  It kept all the other columns as feature columns.
     * The second model had 3 hidden layers, with a mix of ReLu and Sigmoid activation functions.  There were 446 neurons in the input layer and 1 neuron in the output layer.  The first hidden layer had 80 neurons with a ReLu activation function. The second hidden layer had 60 neurons with a Sigmoid activation function.  The third hidden layer had 40 neurons with a Sigmoid activation function.  The number of neurons in the hidden layers were chosen to because they were ~2/3 of the size of the input layer.  Also the number of neurons in the hidden layers are between the size of the input layer and the size of the output layer.
![Screenshot 2024-05-22 163621](https://github.com/imzxtingi/deep-learning-challenge/assets/150073701/fafbbd34-f9f6-4435-b635-f49620d1c239)
   * The second model had an accuracy predictor of 79% and loss of 46% which is better than the first model, however could still be improved to get more accuracy and less loss.
![Screenshot 2024-05-22 163634](https://github.com/imzxtingi/deep-learning-challenge/assets/150073701/d930de39-b991-4822-a18f-1551011a51a8)
  * Some attempts to increase model performance included changing the activation functions from ReLu to Sigmoid.  I found that having all the hidden layers be a ReLu activation function provided similar accuracy but increase in loss, therefore I chose to include Sigmoid activation functions to reduce the amount loss.  Also, I included the NAME column into the training dataset to get the accuracy beyond 75%.  When trying to manipulate just the number of neurons and hidden layers of the model, the optimization was still less than 75%.  Once I included the NAME column, the model had better accuracy.  The second model was able to achieve target model performance. 

## Summary
Overall, Model 2 did better at predicting charity funding for Alphabet Soup.  It had about 79% accuracy which was an improvement from the first model.  A different model that could be used for this classification problem could be a Decision Tree model.  A Decision Tree model is great at classification problems.  Alphabet Soup was looking at whether a organization would be successful with their funding which is a problem that the Decision Tree could tackle. 

## References
**Resources:** The number of neurons and layers were determined by the general rule of thumb outlined in the following StackExchange post.
- [StackExchange](https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw)


