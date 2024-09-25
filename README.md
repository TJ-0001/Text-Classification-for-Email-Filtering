# Text-Classification-for-Email-Filtering
Objective
The purpose of this project was to build an automatic email classification model that categorizes emails into "Spam" and "Important" to enhance email management efficiency. The key goal was to reduce the need for manual sorting of emails.

Findings and Model Results
Data Preprocessing: 

The dataset was cleaned by addressing missing values and performing text preprocessing. The Subject and Body of each email were combined and cleaned (lowercased, punctuation removed, stop words excluded).

Feature Extraction:

TF-IDF (Term Frequency-Inverse Document Frequency) was selected to represent email text. This method helped highlight important words and filter out common but less informative words.
A maximum of 1,000 features was chosen to maintain model simplicity while capturing key patterns.

Model Selection:

A Logistic Regression model was trained on the preprocessed and vectorized text data. Logistic Regression was chosen for its simplicity and interpretability.

Performance:

The model achieved a high accuracy and performed well in terms of precision and recall for "Important" emails.
The confusion matrix revealed that while the model generally distinguished between "Spam" and "Important" emails, some borderline emails were misclassified.

Key Metrics:

Accuracy: 0.92%

Precision: 0.87% for "Important" emails

Recall: 1.0% for "Important" emails

F1 Score: 0.93%

Key Insights

Top Indicators: 

Certain words such as "project", "meeting", and "schedule" were strong indicators of "Important" emails, while "free", "win", and "discount" were commonly associated with "Spam."

Balanced Data: 

The split between "Spam" and "Important" emails was relatively balanced, which contributed to the model's overall performance.

Recommendations for Model Improvement

Expand Feature Set:

Increasing the number of features in the TF-IDF vectorizer may help capture more subtle differences between emails.

Try Advanced Models:

Models like Support Vector Machines (SVM) or Random Forest could potentially enhance performance on ambiguous cases.

Incorporate Additional Features:

Additional metadata such as email sender information, timestamps, or email headers could improve the classification of borderline cases.

Use of Deep Learning:

Consider experimenting with neural networks or LSTM models to capture sequential dependencies in email text, which might enhance the model's understanding of context.

Limitations

Ambiguous Language:

The model struggled with emails where the language was ambiguous, such as promotions that resembled personal messages. This led to some misclassifications.

Limited Context:

The model relies purely on email content (subject and body), missing out on other contextual clues like sender history, which could improve classification accuracy.

Small Dataset:

A larger, more diverse dataset would improve model generalization, especially in capturing more nuanced or uncommon email patterns.

Conclusion

The email classification model built using Logistic Regression and TF-IDF performed well in distinguishing between "Spam" and "Important" emails. Future iterations of this project could focus on improving accuracy by exploring advanced models, expanding feature sets, and incorporating additional data sources.
