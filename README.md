## Introduction
This project implements a deep neural network for machine translation from Kinyarwanda to English using Recurrent Neural Networks (RNNs). It demonstrates the application of sequence-to-sequence models in natural language processing tasks.

## Background
Language translation is crucial in our interconnected world, bridging communication gaps across cultures and nations. With nearly 7,000 different languages worldwide, translation technology plays a vital role in various sectors including business, commerce, media, education, and government.
Recent advancements in deep learning have significantly improved translation quality. This project leverages these advancements by implementing an RNN for Kinyarwanda to English translation.

## Approach
We build a recurrent neural network (RNN) to translate English text to Kinyarwanda. RNNs are particularly suited for NLP tasks due to their ability to process sequences of text as inputs and outputs.

## Dataset Creation and Preprocessing
# Dataset Source:
A custom dataset of English-Kinyarwanda sentence pairs was used.
# Preprocessing Steps:
Text cleaning: Removal of special characters and conversion to lowercase.
Tokenization: Sentences are split into individual words using TensorFlow's Tokenizer.
Vocabulary creation: Unique tokens are collected to form
Padding: Sequences are padded to ensure uniform length using TensorFlow's pad_sequences.
Model Architecture and Design Choices
Model Type:
Sequence-to-sequence architecture with attention mechanism
Components:
Encoder:
Single-layer GRU (Gated Recurrent Unit) with 256 hidden units
Decoder:
Single-layer GRU with 256 hidden units
Dense layer for output prediction
Embedding Layer:
Used for both encoder and decoder inputs
Embedding dimension: 256
Attention Mechanism:
Bahdanau attention implemented
Design Choices:
GRU units were chosen over LSTM for their simplicity and efficiency.
The model is compiled with the Adam optimizer and sparse categorical cross-entropy loss function.
## Training Process and Hyperparameters
# Training Configuration:
Optimizer: Adam with learning rate of 0.001
Loss Function: Sparse Categorical Crossentropy
Batch Size: 64
Epochs: 20 (with early stopping implemented)
Validation Split: 20% of the data
Framework: Keras with TensorFlow
# Evaluation Metrics and Results
# Metrics Used:
BLEU Score (on test sentences)
# Results:
BLEU Score: 0.7
## Insights and Potential Improvements
The model performs well on short sentences but struggles with longer and more complex sentences.
Adding more data and using a more complex model (e.g., Transformer) might improve performance.

## Conclusion
This project successfully implemented an English to Kinyarwanda translation model using a sequence-to-sequence architecture with attention mechanism. The model demonstrates the potential for neural machine translation in low-resource languages. Future work will focus on enhancing model capabilities, expanding the dataset, and implementing more advanced techniques to improve translation quality.

