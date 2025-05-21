# SpamDetection
1: Label: ‘spam’ or ‘ham’
Text Cleaning & Normalization
* Converted text to lowercase
* Removed punctuation
* Removed stopwords (like "the", "and", "is", etc.)
* Applied stemming using PorterStemmer to reduce words to their root form (e.g., "running" → "run"

Used TfidfVectorizer to convert text into numerical format:
* TF (Term Frequency): Frequency of word in a message
* IDF (Inverse Document Frequency): Rarity of the word across all messages
This helps the model understand the importance of each word.


Model Building
Train-Test Split
* Split data into training and test sets (usually 80:20 or 70:30)
Models Used
Several models were trained and evaluated:
1. Multinomial Naive Bayes
    * Good for text classification
    * Assumes features are conditionally independent
2. Logistic Regression
    * Predicts probabilities between 0 and 1
    * Good baseline for binary classification
3. Support Vector Machine (SVM)
    * Effective in high-dimensional spaces
    * Good for separating classes with clear margins
4. Random Forest
    * Ensemble method combining decision trees
    * Robust and handles overfitting well


Model Evaluation
Metrics Used
* Accuracy: Overall correctness
* Precision: How many predicted spams were actually spam
* Recall: How many actual spams were correctly detected
* F1 Score: Balance between precision and recall
* Confusion Matrix: TP, FP, FN, TN values
Best Model: Typically, Multinomial Naive Bayes or SVM performs best in spam detection due to their suitability for text data.

6. Prediction
* The model was tested on new email texts.
* Users can input a message, and the model predicts whether it’s Spam or Ham.
