Text Classification

Abstract:
Text classification is the process of assigning tags or categories to text according to its content. It’s one of the fundamental tasks in Natural Language Processing (NLP) with broad applications such as sentiment analysis, topic labeling, spam detection, and intent detection.
Unstructured data in the form of text is everywhere: emails, chats, web pages, social media, support tickets, survey responses, and more. Text can be an extremely rich source of information
Text classification is becoming an increasingly important part of businesses as it allows to easily get insights from data and automate business processes.

Introduction:
Text classification with machine learning learns to make classifications based on past observations. By using pre-labeled examples as training data, a machine learning algorithm can learn the different associations between pieces of text and that a particular output (i.e. tags) is expected for a particular input (i.e. text).
The first step towards training a classifier with machine learning is feature extraction: a method is used to transform each text into a numerical representation in the form of a vector. One of the most frequently used approaches is bag of words, where a vector represents the frequency of a word in a predefined dictionary of words.
Data Preprocessing:
Whenever we have textual data, we need to apply several preprocessing steps to the data to transform words into numerical features that work with machine learning algorithms.
    1. Remove text lowercase.
    2. Remove numbers.
    3. Remove punctuation.
        ◦ We remove punctuations so that we don’t have different forms of the same word. If we don’t remove the punctuation, then similar worlds may be treated differently.
    4. Remove extra white spaces.
    5. Remove default stop words.
        ◦ Stop words are words that do not contribute to the meaning of a sentence. Hence, they can safely be removed without causing any change in the meaning of the sentence.

    6. Lemmatization.
        ◦ Lemmatization converts a word to its root form and it ensures that the root word belongs to the English language. We will get valid words if we use lemmatization. In NLTK, we use the WordNetLemmatizer to get the lemmas of words. We also need to provide a context for the lemmatization. So, we add the part-of-speech as a parameter.

we will split the dataset into training and validation sets so that we can train and test classifier. Also, we will encode our target column so that it can be used in machine learning models.

Methodology:

 Feature Engineering:  Feature Engineering in which the raw dataset is transformed into flat features which can be used in a machine learning model. This step also includes the process of creating new features from the existing data.

Count Vectors as features:
Count Vector is a matrix notation of the dataset in which every row represents a document from the data, every column represents a term from the data, and every cell represents the frequency count of a particular term in a particular document.
TF-IDF Vectors as features
TF-IDF score represents the relative importance of a term in the document and the entire corpus. TF-IDF score is composed by two terms: the first computes the normalized Term Frequency (TF), the second term is the Inverse Document Frequency (IDF), computed as the logarithm of the number of the documents in the corpus divided by the number of documents where the specific term appears.
TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document)
IDF(t) = log_e(Total number of documents / Number of documents with term t in it)
TF-IDF Vectors can be generated at different levels of input tokens (words, characters, n-grams)
Word Level TF-IDF : Matrix representing tf-idf scores of every term in different documents

Implementing a naive bayes model using sklearn implementation with different features
- Count Vectors
- Word Level TF IDF
Naive Bayes is a classification technique based on Bayes’ Theorem with an assumption of independence among predictors. A Naive Bayes classifier assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature.
Then we calculate the F1 measure , Precision, Recall 

Logistic regression measures the relationship between the categorical dependent variable and one or more independent variables by estimating probabilities using a logistic/sigmoid function. One can read more about logistic regression .
Then we calculate the F1 measure , Precision, Recall . 

