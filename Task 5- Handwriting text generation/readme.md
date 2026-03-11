# Handwritten Text Generation using Character-Level RNN

## Project Overview:
This project implements a **Character-Level Recurrent Neural Network (RNN)** using LSTM to generate new text based on patterns learned from handwritten text samples.

The model is trained on transcriptions extracted from the **IAM Handwriting Dataset**, which contains sentences originally written by humans in handwritten form. The goal is to learn character patterns and generate new text sequences that resemble the style and structure of the training data.

---

## Dataset:

Dataset Source: IAM Handwriting Dataset

The dataset contains:
- Handwritten text images
- Transcribed text corresponding to those handwritten samples

For this project, the **text transcriptions** were used to train a character-level language model.

Dataset characteristics:
- ~287,000 characters
- English sentences extracted from handwritten documents
- Includes punctuation and varied sentence structures

---

## Project Workflow:

### 1️.) Data Collection:
Handwritten text transcriptions were extracted from the IAM dataset using the HuggingFace datasets library.

### 2️.) Text Preprocessing:
- Combined all sentence transcriptions into a single corpus
- Converted text to lowercase
- Built a character vocabulary from unique characters in the dataset

### 3️.) Sequence Generation:
Training samples were created using a sliding window approach:
- Input sequence length: **40 characters**
- Target: **next character prediction**

This allows the model to learn sequential character patterns.

### 4️.) Model Architecture:

A Character-Level RNN was built using **TensorFlow / Keras**:

- Embedding Layer (character embedding)
- LSTM Layer (128 units)
- Dropout Layer (0.2)
- Dense Output Layer with Softmax activation

The model predicts the probability distribution of the next character.

### 5️.) Model Training:

Training configuration:
- Batch Size: 128
- Epochs: 30
- Loss Function: Sparse Categorical Crossentropy
- Optimizer: Adam

Training results:
- Final Training Accuracy ≈ **59%**
- Final Loss ≈ **1.34**

---

## Text Generation:

After training, the model generates text by:
1. Providing a seed sequence
2. Predicting the next character
3. Appending it to the sequence
4. Repeating the process iteratively

Example generated text:

at a meeting of labour a move to stop mr...
the committee agreed that the resolution...


## The generated output demonstrates that the model learned:
- sentence structure
- punctuation patterns
- word-like formations

---

## Technologies Used:

- Python
- TensorFlow / Keras
- NumPy
- HuggingFace Datasets
- Google Colab

---

## Key Learnings:

- Character-level language modeling using RNNs
- Sequence generation with sliding window technique
- Training LSTM networks for text prediction
- Probabilistic text generation using sampling

---

## Note:

The dataset link provided in the internship task instructions redirected to the HuggingFace **Trending Papers** page instead of a dataset. Therefore, the **IAM Handwriting Dataset** was used via the HuggingFace datasets library to obtain handwritten text transcriptions for training.

---

## Future Improvements:

- Train for more epochs to improve text coherence
- Experiment with deeper LSTM architectures
- Implement temperature-based sampling for better generation
- Use larger handwriting corpora for richer vocabulary
