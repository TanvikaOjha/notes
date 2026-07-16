# Autoregressive Generation
Autoregressive models are a class of statistical models that predict future values based on previous ones. These models generate sequences of words or tokens one step at a time, conditioned on the previously generated tokens. 

We can say that an LLM is a function that accepts text up to a pre-defined vocabulary.

An LLM
1. **Accepts an input context**: LLMs look at their input and output as numbers(tokens). These tokens are the basic unit by which LLMs understand and predict text. The set of all supported values of these tokens is called model's vocabulary.

When you prompt an LLM, the prompt undergoes tokenization.
2. **Predicts a single token out of a vocabulary**: Also known as generating a completion for the input context.

When an LLM figures out the meaning of its input context, it provides probability distribution over it's vocabulary.We don't simply choose the token with highest probability and isn't even the most reasonable one from the AI/Human alingment perspective. Instead we choose one using various sampling techniques that introduce randomization into the choice process, while respecting the assigned probabilities.

3. **Feeds that token back into the input context**: the newly generated token is appended to the end.
4. **Repeats the process again until something tells it to stop**:  the iterative feed-back loop is directly related to how autoregressive models are trained. During the training process, they are asked to predict or fill out the next token in the context. Once they improve on that the training process moves on to the next token, and so forth.

## Sampling Techniques
- **Greedy Decoding**: It always picks the word with the highest probability. Great for task where factual answers are required(math problem, code genration)
- **Temperature Scaling**: This method adjusts the sharpness of the probability scores before selection. High temperature flattens the odds, giving unlinkely words a better chance.(for creative writing=>high temp, strict tasks => low temp)
- **Top-K Sampling**: instead of choosing from all possible words, this method only looks for top K words and ignores the rest. Then, it splits the probability fairly among those remaining words. it prevents the model from choosing bizzaew or gramatically incorrect words while keeping the text somewhat diverse.
- **Top-p(Nucleus) Sampling**: The model sorts words by probability and adds them to the list one by one until the total probability equals a set percentage. It then samples only from this restricted list. 

# Key Charachterisitics of Autoregressive models
- **Sequential Generation**: Words are generated one after another.
- **Conditional Probability**: each word is predicted using conditional probability distribution given the prior context. 
- **Markov Property**: The prediction for the current word depends only on the immediate history(previous words), not the entire sequence.

# Applications of Autoregressive models
1. Text Generation
2. Machine Translation
3. Speech Recognition
4. Text Summarization
5. Dialouge Systems