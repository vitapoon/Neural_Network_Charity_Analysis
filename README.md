# Neural_Network_Charity_Analysis

## Overview of the analysis

With the knowledge of machine learning and neural networks, i’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. This project is comprised of 3 steps: Preprocessing the data for the neural network, Compile,train and evaluate the model & finally optimizing the model.

## Results

### Data Preprocessing

After looking at the data, I established that the target variable is the "IS_SUCCESSFUL" column. I then removed the "EIN" and "NAME" columns as they did not offer any relevant data that could help the model perform better. The remaining columns became the features for the model.

### Compiling, Training, and Evaluating the Model

For my first attempt at compiling a neuron network consisted of 80 neurons in the first layer and 30 in the second. Both layers had relu activation functions and the output layer had a sigmoid activation function. I started with these parameters as relu does better with nonlinear data, and two layers allows for a second layer to reweight the inputs from the first layer. Here are the preformance metrics of this model.

268/268 - 0s - loss: 0.5538 - accuracy: 0.7335
Loss: 0.5537912845611572, Accuracy: 0.7335277199745178

In my second attempt, I removed the "SPECIAL_CONSIDERATIONS" column. Here are the preformance metrics of this model.

268/268 - 1s - loss: 0.5656 - accuracy: 0.7275
Loss: 0.5656009316444397, Accuracy: 0.7274635434150696

In my third attempt, I remove more noisy variables['AFFILIATION_CompanySponsored', 'AFFILIATION_Family/Parent','AFFILIATION_Independent', 'AFFILIATION_National', 'AFFILIATION_Other',
'AFFILIATION_Regional','USE_CASE_Heathcare', 'USE_CASE_Other', 'USE_CASE_Preservation','USE_CASE_ProductDev']. 

Add more Hidden Layers and change the activation from "relu" to "sigmoid". Here are the preformance metrics of this model.Here are the preformance metrics of this model.

268/268 - 0s - loss: 0.6214 - accuracy: 0.6574
Loss: 0.6213651299476624, Accuracy: 0.6573761105537415


### Summary
After four attempts, I was unable to create a model that could preform a 75% accuracy rating. This is potential becasue I got rid of too many columns, I did not use the correct activation function, or I did not have hte right amount of layers and neurons. These were the main areas I continued the change with little to no improvement. May I know what should I do to get the accuracy rate up to 75%?
