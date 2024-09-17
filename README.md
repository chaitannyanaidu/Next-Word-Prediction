# Next-Word-Prediction

Developed a Next Word Prediction system using a Bidirectional Long Short-Term Memory (Bi-LSTM) model. 
The model was trained on large text corpora to predict the most likely next word given a sequence of words,
enhancing natural language processing capabilities.
Demonstrated proficiency in deep learning techniques and model deployment for text generation tasks.






![image](https://github.com/user-attachments/assets/e150d6f3-0be8-462b-8e8e-caae157aba1a)





# 1. Data Preprocessing

- Tokenization: Split the input text into individual words (tokens).
- Vocabulary Creation: Build a vocabulary of unique words and assign a numerical ID to each word.
- Text Vectorization: Convert text into numerical sequences using word IDs.
- Padding: Ensure all sequences have equal length by adding padding tokens (usually zeros).

## 2. Model Architecture

### Bidirectional LSTM Layer

- Processes input sequences in both forward and backward directions.
- Each direction has its own LSTM layer.
- Captures contextual information from both past and future words.

### Concatenation Layer

- Combines outputs from forward and backward LSTM layers.
- Creates a more comprehensive representation of the sentence.

### Dense Output Layer

- Maps the concatenated output to the size of the vocabulary.
- Produces a probability distribution over the possible next words.

## 3. Model Training

- Input: Sequences of words, where the last word is masked as the target for prediction.
  
### Forward Pass

- The Bidirectional LSTM processes the sequence in both directions.
- The concatenated output is fed to the dense layer for prediction.

### Loss Calculation

- The model compares the predicted probabilities with the actual next word using a loss function (e.g., categorical cross-entropy).

### Backpropagation

- Adjusts the model weights to minimize the prediction error.

## 4. Prediction

- Input: A partial sentence (sequence of words).
  
### Forward Pass

- The model processes the input sequence to predict the next word.

### Output

- Produces a probability distribution over the possible next words.

### Word Selection

- Select the word with the highest probability or sample from the distribution.

## Key Points

- Bidirectional LSTM: Captures both past and future context, improving prediction accuracy.
- Training: Involves iteratively adjusting model weights to minimize prediction errors.
- Prediction: Generates a probability distribution over possible next words based on input sequences.

## results

![image](https://github.com/user-attachments/assets/ca333f42-75af-4e8b-82bf-e9ad6a099e5c)


![image](https://github.com/user-attachments/assets/33401365-d56d-4401-94bc-b14dd15074b7)






