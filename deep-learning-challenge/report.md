# Alphabet Soup Neural Network Report

## Overview
The neural network constructed in the associated notebooks seeks to produce a reliable predictive model as it relates to the success of charity organizations.

The neural network aggregates several related features per organization to attempt to predict the organization's success as a binary decision (successful or not successful).

## Results
- ### Data Preprocessing
    - The target of the model was the success of the organization as a binary outcome (successful or not successful).
    - The features used by the model were the application type, sector of industry, government organization classification, case for funding, organization type, and funding amount requested.
    - The identification and name of the organization were not considered, initially, as they should in theory hold no weight in determining success. However, as will be discussed later, the name was reintroduced as a categorical variable.

- ### Compiling, Training, and Evaluation
    - The current model contains three hidden layers. Layer one has a rectified linear unit (relu) activation with 15 neurons, layer two has an exponential linear unit (elu) activation with 20 neurons, and layer three has a relu activation with 20 neurons.
    - Target performance of 0.75 was able to be reached.
    - Attempts were made to optimize performance through several means. First, removing special consideration, while also adding and rebinning organization names. This was done as it was determined through repeated testing that special consideration did not benefit the model accuracy, whereas the organization name was a value which was not unique unlike the identification number, this meant it was possible to rebin the names to add more depth to the data. Secondly, the number of neurons was reduced across all layers. This was done to balance efficiency as well as results. Finally, the number of hidden layers as well as activation functions were adjusted to account for the complexity of the data.


## Summary
Overall, the neural networks performance is only good. It is not an exceptional predictor in its current form, but further tuning may reveal a more optimal set up. However, it may also be more beneficial to use a random forest classifier. The current dataset is quite small and therefore a simple machine learning model may prove optimal. Due to the binary nature of the problem, as well as several features which may have direct relationships to the target, a decision tree may be a more direct and efficient route.