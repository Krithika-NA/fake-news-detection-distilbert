# Fake News Detection using DistilBERT

## Project Overview
This project builds a Fake News Detection system using a pretrained Transformer model (DistilBERT). The model is fine-tuned on a real fake news dataset to classify news articles as Fake or Real.

## Model
DistilBERT (distilbert-base-uncased)

## Dataset
Fake and True news dataset containing ~44,000 news articles.

## Methodology
1. Data preprocessing and cleaning
2. Tokenization using DistilBERT tokenizer
3. Train-test split
4. Fine-tuning DistilBERT for sequence classification
5. Evaluation using Accuracy, Precision, Recall, F1-score
6. Confusion Matrix analysis

## Results
Accuracy: 1.00  
Precision: 1.00  
Recall: 1.00  
F1-score: 1.00

## Demo
A Gradio interface allows users to input news text and receive predictions with confidence scores.

## Technologies Used
- Python
- Transformers (HuggingFace)
- PyTorch
- Scikit-learn
- Gradio


