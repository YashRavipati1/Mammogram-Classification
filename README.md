# Mammogram-Classification

Designed and trained a logistic regression model to predict whether a mammogram mass from the UCI "mammographic masses" public dataset was benign or malignant. The model was trained on 5 features:

1. BI-RADS assessment: 1 to 5 (ordinal)
2. Age: patient's age in years (integer)
3. Shape: mass shape: round=1 oval=2 lobular=3 irregular=4 (nominal)
4. Margin: mass margin: circumscribed=1 microlobulated=2 obscured=3 ill-defined=4 spiculated=5 (nominal)
5. Density: mass density high=1 iso=2 low=3 fat-containing=4 (ordinal)

I decided on logistic regression after multiple trials with other models. The models' k-fold cross validation accuracy values are as follow:

  Keras Deep Learning Model (binary output neuron, binary cross entropy loss function, ADAM optimizer, RELU activation function): 80.36%
  Decision Trees: 73.98%
  Random Forest Classifier: 75.66%
  Support Vector Classification (Linear Kernel): 79.76%
  Support Vector Classification (rbf Kernel): 80.12%
  Support Vector Classification (Sigmoid Kernel): 74.58%
  Support Vector Classification (Poly Kernel): 79.03%
  K-Nearest Neighbors (Attempted with values of K from 1 to 50 - Highest accuracy achieved with K = 7): 79.63%
  Naive Bayes: 78.55%

I attempted using a number of different toploogies and hyperparameters for the deep learning model. However, in every situation, the logistic regression model proved to be more efficient with a higher cross-validation accuracy. The final logistic regression accuracy was 80.72%.
