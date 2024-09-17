# Next-Word-Prediction

Developed a Next Word Prediction system using a Bidirectional Long Short-Term Memory (Bi-LSTM) model. 
The model was trained on large text corpora to predict the most likely next word given a sequence of words,
enhancing natural language processing capabilities.
Demonstrated proficiency in deep learning techniques and model deployment for text generation tasks.



![image](https://github.com/user-attachments/assets/e150d6f3-0be8-462b-8e8e-caae157aba1a)



Here's a breakdown of the algorithm for using bidirectional LSTM in next word prediction:
1. Data Preprocessing:
●	Tokenization: Split text into individual words (tokens).
●	Vocabulary Creation: Build a vocabulary of unique words and assign each word a numerical ID.
●	Text Vectorization: Transform text into numerical sequences using word IDs.
●	Padding: Ensure sequences have equal length by adding padding tokens (usually zeros).
2. Model Architecture:
●	Bidirectional LSTM Layer:
○	Processes input sequences in both forward and backward directions.
○	Each direction has its own LSTM layer.
○	Captures contextual information from both past and future words.
●	Concatenation Layer:
○	Combines outputs from forward and backward LSTM layers.
○	Creates a more comprehensive representation of the sentence.
●	Dense Output Layer:
○	Applies a final transformation to map the concatenated output to the vocabulary size.
○	Produces a probability distribution over possible next words.
3. Model Training:
●	Input: Sequences of words, where the last word is masked (target to predict).
●	Forward Pass:
○	Bidirectional LSTM processes the sequence in both directions.
○	Concatenated output is fed to the dense output layer.
●	Loss Calculation:
○	Compare predicted probabilities with actual next word using a loss function (e.g., categorical cross-entropy).
●	Backpropagation:
○	Adjust model weights to minimize the loss.
4. Prediction:
●	Input: A partial sentence (sequence of words).
●	Forward Pass:
○	Model processes the input sequence.
●	Output: Probability distribution over possible next words.
●	Selection:
○	Choose the word with the highest probability or sample from the distribution.
Key Points:
●	Bidirectional LSTMs capture both past and future context for more accurate predictions.
●	Training involves iteratively adjusting weights to minimize prediction errors.
●	Prediction involves generating a probability distribution over possible next words.
