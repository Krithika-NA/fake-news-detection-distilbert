# Fake News Detection using DistilBERT

## Problem Statement
The rapid spread of misinformation and fake news on the internet has become a significant challenge. Detecting fake news manually is difficult due to the large volume of content generated daily. The goal of this project is to build a machine learning model that can automatically classify news articles as **Fake** or **Real** using Natural Language Processing (NLP) techniques and transformer-based models.

---

## Approach
The project follows a typical NLP pipeline:

1. **Dataset Preparation**
   - Used the Kaggle Fake News Dataset containing Fake and True news articles.
   - Combined both datasets and assigned labels:
     - `0 → Fake News`
     - `1 → Real News`

2. **Data Preprocessing**
   - Merged the `title` and `text` fields to create a single input feature.
   - Shuffled the dataset to remove ordering bias.

3. **Tokenization**
   - Used the HuggingFace DistilBERT tokenizer.
   - Applied padding and truncation with a maximum sequence length of **512 tokens**.

4. **Train-Test Split**
   - Split dataset into **80% training** and **20% validation**.

5. **Model Training**
   - Fine-tuned a pretrained transformer model for sequence classification.

6. **Evaluation**
   - Evaluated model performance using standard classification metrics.

7. **Deployment**
   - Built a simple **Gradio interface** where users can input news text and receive predictions.

---

## Model Used
The model used in this project is **DistilBERT (distilbert-base-uncased)** from the HuggingFace Transformers library.

DistilBERT is a lightweight version of BERT created through knowledge distillation. It maintains strong language understanding capabilities while reducing model size and computational cost.

Key characteristics:
- Approximately **66 million parameters**
- About **40% smaller than BERT**
- Around **60% faster than BERT**

This makes DistilBERT suitable for efficient training and deployment.

---

## Evaluation Metrics
The trained model was evaluated on the validation dataset using the following metrics:

| Metric | Score |
|------|------|
| Accuracy | 1.00 |
| Precision | 1.00 |
| Recall | 1.00 |
| F1 Score | 1.00 |

The confusion matrix confirmed that all validation samples were correctly classified.

---

## Model Improvements
To improve efficiency, **DistilBERT was chosen instead of the standard BERT model**.

Comparison:

| Feature | BERT | DistilBERT |
|------|------|------|
| Model Size | Larger | Smaller |
| Parameters | ~110M | ~66M |
| Training Speed | Slower | Faster |
| Memory Usage | Higher | Lower |

DistilBERT provides similar performance while significantly reducing computational requirements.

---

## Key Learnings
Through this project, several important concepts were learned:

- Understanding the workflow of transformer-based NLP models.
- Using pretrained models from the HuggingFace Transformers library.
- Applying tokenization and sequence preprocessing for NLP tasks.
- Fine-tuning transformer models for text classification.
- Evaluating model performance using classification metrics.
- Deploying machine learning models with a simple interactive interface using Gradio.

This project demonstrates how transformer-based models can be effectively applied to real-world problems such as fake news detection.

---
