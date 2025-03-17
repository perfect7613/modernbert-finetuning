# ModernBERT-based Phishing Site Classification

This project demonstrates how to fine-tune a ModernBERT model for classifying websites as phishing or safe using the Hugging Face Transformers library.

## Dataset

The project uses the "shawhin/phishing-site-classification" dataset from Hugging Face Datasets.

## Model

ModernBERT is a modernized bidirectional encoder-only Transformer model (BERT-style) pre-trained on 2 trillion tokens of English and code data with a native context length of up to 8,192 tokens.

## Fine-tuning

The following steps are performed for fine-tuning:

1. Load the dataset using `datasets.load_dataset`.
2. Load the pre-trained ModernBERT model and tokenizer using `AutoModelForSequenceClassification` and `AutoTokenizer`.
3. Freeze the base model parameters and unfreeze the pooling layers.
4. Preprocess the text data using the tokenizer.
5. Create a data collator for padding.
6. Define evaluation metrics (accuracy and ROC AUC).
7. Set up training arguments, including learning rate, batch size, and number of epochs.
8. Create a Trainer instance and train the model.
9. Evaluate the model on the validation set.
10. Push the trained model to the Hugging Face Model Hub.
