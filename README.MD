# Machine Learning Model for Amazon Mobile Phone Reviews
This is a Machine Learning (ML) model that analyzes Amazon mobile phone reviews. It uses a pipeline to preprocess the text and fit a classifier, allowing it to make predictions on new reviews.

# Prerequisites
Python 3.x
Pandas
Seaborn
Matplotlib
Scikit-Learn
Joblib

# Dataset
This model uses the Amazon_Unlocked_Mobile.csv dataset which contains reviews of mobile phones sold on Amazon. The dataset is read in using the pd.read_csv() function from the Pandas library.

# Data Preprocessing
The clean_text() function is defined to preprocess the text data in the "Reviews" column. This function converts the text to lowercase and removes punctuation using the str.translate() and str.maketrans() functions from the string library. The clean_text() function is applied to the "Reviews" column using the apply() method.

# Model Training
The dataset is split into training and testing sets using the train_test_split() function from Scikit-Learn. The Pipeline class is used to create a pipeline that preprocesses the text and fits a classifier. Different vectorizers, such as CountVectorizer() and TfidfVectorizer(), and classifiers, such as MultinomialNB(), LogisticRegression(), DecisionTreeClassifier(), and RandomForestClassifier(), can be tried and tested to see which ones perform better.

# Model Evaluation
The model's accuracy is calculated using the accuracy_score() function from Scikit-Learn. The predicted ratings and actual ratings are plotted using the matplotlib.pyplot library. Finally, the model is saved using the dump() function from Joblib, which can be used to load the model for future use.

# Usage
To use this model, ensure that you have installed all the necessary libraries. Then, you can run the script and adjust the vectorizer and classifier in the pipeline to suit your needs. After training, the model can be used to make predictions on new reviews. To load the model for future use, simply call the load() function from Joblib.