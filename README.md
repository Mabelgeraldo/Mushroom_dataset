# Mushroom_dataset
Introduction:
This project focuses on building a classification model to determine the edibility of mushrooms based on their characteristics. The dataset used in this project contains information about various features of mushrooms and their corresponding labels indicating whether they are edible or poisonous.

Objective:
The primary objective of this project is to create an accurate machine learning model that can predict whether a mushroom is edible or poisonous based on its features. To achieve this, the project employs the K-Nearest Neighbors (KNN) algorithm for classification and addresses class imbalance using Synthetic Minority Over-sampling Technique (SMOTE).

Project Workflow:

    Data Loading: The project begins by loading the mushroom dataset using the Pandas library.

    Data Exploration:
        The dataset is explored to understand its structure and contents.
        An initial check is performed to identify if any columns contain missing data represented as question marks.

    Data Preprocessing:
        Columns containing question marks are identified to determine if they need further processing.
        Question marks in the dataset are replaced with NaN values to standardize missing data representation.
        Columns with missing values are identified, and the missing values are handled by replacing them with the mode (most frequent value) of the "stalk-root" column.
        The label column, "class," is encoded using the LabelEncoder to convert class labels into numeric format.
        Categorical features are one-hot encoded to convert them into numerical format, making them suitable for machine learning models.

    Handling Class Imbalance:
        Class imbalance is addressed using the Synthetic Minority Over-sampling Technique (SMOTE). This technique generates synthetic samples of the minority class to balance the class distribution.

    Data Splitting:
        The data is split into training and testing sets for model development and evaluation.
        A typical split ratio of 80% for training and 20% for testing is used.

    K-Nearest Neighbors (KNN) Classification:
        A K-Nearest Neighbors classifier is chosen as the classification algorithm.
        Hyperparameter tuning is performed using GridSearchCV to find the optimal combination of hyperparameters (number of neighbors, weighting scheme, distance metric) for the KNN model.
        GridSearchCV uses 5-fold cross-validation to assess model performance.

    Model Evaluation:
        The KNN classifier with the optimal hyperparameters is trained on the training data.
        Predictions are made on the test data, and model performance is evaluated using accuracy, classification report, and other relevant metrics.
        The accuracy metric measures the overall correctness of the model's predictions.
        The classification report provides additional insights into precision, recall, and F1-score for each class.

Conclusion:
The project concludes with the evaluation of the K-Nearest Neighbors classifier's performance in classifying mushrooms as edible or poisonous. The use of SMOTE to address class imbalance contributes to a more robust model, and hyperparameter tuning enhances its predictive accuracy. The project provides valuable insights into the classification of mushrooms for potential applications in mycology and food safety.
