# Sentiment Analysis with IMDB Dataset

## Guide
Ishant Gupta

## Submitted By
Shanmuga Priyan Jeevanandam (C0889053)

## Introduction
Sentiment Analysis is a Natural Language Processing (NLP) technique used to determine whether a piece of text (like a movie review, tweet, or news article) expresses a positive, negative, or neutral sentiment. This project utilizes Recurrent Neural Networks (RNNs) to perform sentiment analysis on the IMDB dataset, which contains 50,000 movie reviews labeled as positive or negative.

## Objectives
1. Understand sentiment analysis and RNNs.
2. Prepare the IMDB dataset for model training.
3. Build and train an RNN model.
4. Implement a simple feedforward neural network (FFN) for comparison.
5. Evaluate the performance of both models.
6. Provide insights and conclusions from the analysis.

## 1. Understanding Sentiment Analysis and RNNs

### What is Sentiment Analysis?
Sentiment analysis involves determining the sentiment expressed in text. It has various applications:
- **Social Media Monitoring:** Assessing public opinion on social platforms.
- **Customer Feedback Analysis:** Evaluating customer reviews for products and services.
- **Market Research:** Understanding consumer sentiment towards brands or products.
- **Political Analysis:** Gauging public sentiment on political issues or figures.

### How RNNs Differ from Traditional Feedforward Neural Networks
- **Structure:** Traditional feedforward neural networks process inputs in a single pass, whereas RNNs have loops that allow information to persist.
- **Memory:** RNNs maintain a 'memory' through hidden states, enabling them to handle sequential data effectively, unlike feedforward networks that treat each input independently.

### Concept of Hidden States and Information Passing in RNNs
- **Hidden States:** At each time step, an RNN takes an input and a hidden state from the previous time step and produces an output and a new hidden state. This hidden state acts as a memory of previous inputs.
- **Information Passing:** The hidden state is updated iteratively, allowing the network to capture temporal dependencies in the data.

### Common Issues with RNNs
- **Vanishing Gradients:** Gradients used for updating weights become very small, causing the model to stop learning.
- **Exploding Gradients:** Gradients become excessively large, causing unstable updates.

## 2. Dataset Preparation

### Key Steps:
1. **Loading Dataset:** IMDB dataset with a vocabulary size of 10,000 words.
2. **Padding Sequences:** Ensuring all sequences are of equal length (200 words).
3. **Splitting Dataset:** Creating training and validation sets.

## 3. Building the RNN Model

### Key Components:
1. **Embedding Layer:** Converts word indices into dense vectors of fixed size.
2. **LSTM Layer:** Long Short-Term Memory units with dropout for regularization.
3. **Dense Layer:** Single neuron with sigmoid activation for binary classification.

### Training the Model
- **RNN Test Accuracy:** Achieved an accuracy of around 85% on the test set.

### Training and Validation Accuracy and Loss:
*Include relevant charts or graphs here.*

## 5. Simple Feedforward Neural Network Implementation

### Results:
- **FFN Test Accuracy:** Achieved an accuracy of around 85% on the test set.

### Training and Validation Accuracy and Loss:
*Include relevant charts or graphs here.*

## 6. Evaluating the Model

### Observations:
- **RNN Model:** Consistently performs well on sequential data, capturing temporal dependencies.
- **FFN Model:** Despite its simplicity, it performs comparably on this task.

## 7. Hyperparameter Tuning

### Key Changes:
- **Learning Rate Adjustment:** Changed to 0.001 for potentially better convergence.

## 8. Comparative Analysis

### Simple Feedforward Network:
- **FFN Test Accuracy:** Around 85%, similar to RNN.

## Conclusion
This project demonstrated the effectiveness of Recurrent Neural Networks (RNNs) in handling sequential data for sentiment analysis tasks. Both RNN and simple feedforward neural networks (FFN) achieved comparable accuracies on the IMDB dataset. RNNs excel in capturing temporal dependencies in the data, while FFNs, despite their simplicity, can perform well on specific tasks. Hyperparameter tuning and early stopping played crucial roles in optimizing model performance.

### Insights:
1. RNNs are suitable for sequential data due to their memory capabilities.
2. FFNs can serve as strong baselines for comparison.
3. Regularization and Dropout are essential to prevent overfitting.
4. Early Stopping helps in selecting the best model during training.

Overall, this project provided valuable experience in applying RNNs to real-world NLP tasks and highlighted the importance of model selection and hyperparameter tuning.
