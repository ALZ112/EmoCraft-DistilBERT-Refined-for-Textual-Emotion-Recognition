<h1> Emotion Detection with DistilBER </h1

Emotion detection is a critical aspect of natural language understanding, with applications ranging from sentiment analysis to mental health monitoring. This report outlines the development, training, and evaluation of an emotion detection model using DistilBERT, a distilled version of BERT.

<h2> _**2. Data Overview**_</h2> 
2.1 Dataset
The dataset used for this project consists of labeled text samples, each annotated with one of four emotion categories: fear, sadness, joy, and anger.

2.2 Data Preprocessing
To prepare the text data for modeling, extensive preprocessing steps were applied:

Removal of HTML tags and syntax.
Elimination of punctuation characters.
Handling of underspace characters.
Removal of digits.
Elimination of links and URLs.
Removal of special characters.
Removal of stopwords.
Conversion of text to lowercase.
Removal of non-ASCII characters.
Removal of email addresses.
3. Model Architecture
_**3.1 DistilBERT Model**___
The selected model architecture is DistilBERT, known for its efficiency and effectiveness in natural language processing tasks. The architecture involves:

Tokenization of text using the DistilBERT tokenizer.
Definition of input layers for input IDs and attention masks.
Passage of input sequences and attention masks through the DistilBERT model.
Extraction of the final hidden states for subsequent processing.
3.2 Training
The training process incorporates early stopping and model checkpointing to prevent overfitting. Tokenized input sequences are fed to the DistilBERT model, optimizing for sequence classification.

3.3 Hyperparameter Tuning
Hyperparameter tuning was performed using the Keras Tuner library. Various configurations, including the number of layers, units per layer, activation functions, dropout rates, and the optimizer, were explored to optimize the DistilBERT-based model.

_**4. Results**_
4.1 Model Performance (Without Fine-Tuning)
4.1.1 Accuracy
Accuracy Score: 0.8592210229938996
4.1.2 Precision
Micro-Averaged Precision Score: 0.8592210229938996
Macro-Averaged Precision Score: 0.8679396176468916
Weighted Precision Score: 0.8625664847936705
4.1.3 Recall
Micro-Averaged Recall Score: 0.8592210229938996
Macro-Averaged Recall Score: 0.8554711326736939
Weighted Recall Score: 0.8592210229938996
4.1.4 F1 Score
Micro-Averaged F1 Score: 0.8592210229938996
Macro-Averaged F1 Score: 0.8604079281821589
Weighted F1 Score: 0.8594579169032848

4.2 Model Performance (With Fine-Tuning)
4.2.1 Accuracy
Accuracy Score: 0.8629751290473956
4.2.2 Precision
Micro-Averaged Precision Score: 0.8629751290473956
Macro-Averaged Precision Score: 0.8722899934191831
Weighted Precision Score: 0.8666208703178802
4.2.3 Recall
Micro-Averaged Recall Score: 0.8629751290473956
Macro-Averaged Recall Score: 0.8586897619786459
Weighted Recall Score: 0.8629751290473956
4.2.4 F1 Score
Micro-Averaged F1 Score: 0.8629751290473957
Macro-Averaged F1 Score: 0.864177036204409
Weighted F1 Score: 		 0.8633345834459296
4.3 Final Model Evaluation
4.3.1 Loss and Accuracy

Test Sparse Categorical Balanced Crossentropy Loss: 1.0297473669052124
Test Balanced Categorical Accuracy: 0.8629751205444336

**_5. Future Work_**
To further enhance the model and its applications:

Explore fine-tuning on domain-specific data.
Investigate ensemble models to improve predictive accuracy.
Develop a user interface for real-time emotion prediction.

_**6. Conclusion**_
The successful implementation of DistilBERT for emotion detection showcases its potential in accurately classifying emotions from text. The combination of an efficient model architecture, hyperparameter tuning, and comprehensive evaluation contributes to improved performance in understanding and classifying textual emotions.
