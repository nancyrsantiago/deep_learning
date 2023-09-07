# deep_learning

Results for Optimized Model

The features that hold the majority of the signal required for the model to achieve the target model performance are:
NAME
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE
ORGANIZATION
INCOME_AMT
ASK_AMT

The features that hold minor to no significance for the model to performance are:
EIN 
STATUS
SPECIAL_CONSIDERATIONS

The target variable that is being predicted is IS_SUCCESSFUL

Compiling, Training, and Evaluating the Model

The Optimized Neural Network Model was defined as follows (see Compiling, Training and Model attachment)

Since a binary classifier needed to be built, the sigmoid activation function was used for the output layer. Sigmoid reduces the output to a value from 0.0 to 1.0, representing a probability.

Since the model achieved the target performance during the first epoch and to reduce the training time per epoch, fewer neurons were used

# Compile the model
nn.compile(loss="binary_crossentropy", optimizer="adam", metrics=["accuracy"])

The binary_crossentropy loss function was used since it is purpose-built for binary classifiers. The metrics was set to ‘accuracy’ so accuracies computed by the loss function are captured in the history object and returned by fit.

The model only trained for ten epochs since the model achieved the target performance during the first epoch and showed little to no improvement in accuracy after the three epochs(see attachment).

One significant change that was added to increase the model performance was adding the NAME feature back as an input during the model optimization. Due to this change, a significant improvement in the model performance was noticed.

Summary: A binary classification model was built using Neural Networks. Before optimizing the model, the accuracy was approximately 73%. However, after optimizing the model, the target performance was achieved with an accuracy of over 79%.
After researching binary classifiers (models that are trained with datasets labeled with 1s and 0s representing the two classes), other popular learning algorithms that do well with binary classification were found, including logistic regression, Naïve Bayes, and k-Nearest Neighbor. Future work of this project would include comparing the performance of the optimized neural network model against the other machine learning models that typically perform well on binary classification.
