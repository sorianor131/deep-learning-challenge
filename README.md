# deep-learning-challenge
Module 21 Homework Assignment - Deep Learning Challenge

## Overview
This report explores the development and fine-tuning of a neural network model designed for the specific task at hand. It delineates the adjustments made to improve the model's effectiveness.

## Results
### Data Preprocessing:

The target variable for this model is the "IS_SUCCESSFUL" column.

The final feature variables included:
* NAME
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* INCOME_AMT
* ASK_AMT

Variables removed from the final model include:
* EIN: Served solely as an identification number.
* SPECIAL_CONSIDERATIONS: Predominantly contained 'N' values with minimal 'Y' occurrences, hence deemed unhelpful.
* STATUS: Featured overwhelmingly more '1' values compared to '0', rendering it uninformative.

### Compiling, Training, and Evaluating the Model:
* The final model comprised three layers with varying neuron counts: 100 in the first layer, 30 in the second, and 10 in the third.

![Optimized Model](Images/Optimized%20Model.png)

* Activation functions utilized were rectified linear units (ReLU) and Sigmoid.

* The model surpassed the targeted performance of 75%, achieving 79% accuracy.

![Accuracy Report](Images/Accuracy%20Report.png)

* Steps taken to enhance model performance included:
    * Inclusion of the NAME column, leveraging the potential correlation between organization names and success.

    * Removal of SPECIAL_CONSIDERATIONS and STATUS columns due to their negligible variability.

    * Addition of a third layer to augment model complexity.

    * Modification of activation functions in the second and third layers.

## Summary
The refined neural network exhibited a notable improvement, achieving 79% accuracy compared to the initial 73%. This enhancement was attributed to strategic modifications, including feature adjustments, layer additions, and activation function alterations. Further refinement could potentially enhance the performance of one or both models, leading to an even more accurate predictive classifier.

# References
* [Colab Save and Load Documentation](https://colab.research.google.com/github/tensorflow/docs/blob/master/site/en/tutorials/keras/save_and_load.ipynb)