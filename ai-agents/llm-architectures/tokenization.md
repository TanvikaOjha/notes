# What is Tokenization?
It is a process of converting a sequence of text into smaller parts, known as tokens. These tokens can be as small as chars or as long as words. It breaks down stretches of text into more digestible and understandable units for machine without losing it's context.

It makes pattern recognition easier.

## Types of Tokenization

Tokens are the building blocks of LLMs.Tokenization methods vary based on the granularity of the text breakdown and the specific requirement at hand.


|Type      | Description| Use Cases|
|----      |----                                      |----                                                           |
|Word Tokenization| Breaks text into individual words.|Effective for languages with clear word boundaries like English|
|Charachter Tokenization|Segments text into individual charachters.|Useful for languages without clear word boundaries or tasks requiring granular analysis.|
|Subword Tokenization | Breaks text into units larger than charachters but smaller than words.| Beneficial for langiages with complex morphology or handling out-of-vocabulary words.|


## Tokenization Usecases
- Search engines
- Machine Translation
- Speech Recognition
- Sentiment analysis in reviews

## Challenges
- Ambiguity
- Languages without clear boundaries
- Special charachters
- Out-of-vocabulary words
- compound words
- multi-word expressions
- domain-specific terms

## Byte-Pair Encoding
A data compression and subword tokenization algorithm. It iteratively merges the most frequently occuring adjacent pairs of charachters or bytes to create new, longer tokens until a predefined vocabulary size is reached.

BPE strikes a balance between charachter-level and word-level tokenization. While char tokenization results in long sequences and word tokenization struggles with rare words, BPE creates meaningful subwords. This allows models to handle unseen words by breaking them down into known subword pieces, which is why it is used in LLMs like GPT, Llama etc.

### How BPE works?
1. **Initialization**: words are splitted into individual charachters.
2. **Frequency Count**: the algo scans the entire training corpus to count the frequency of all adjacent token pairs.
3. **Merging**: The most frequent pair is merged into single, new token.
4. **Vocabulary Update**: The new token is added to the library, and the corpus is updated by replacing the original pair with newly formed token
5. **Iteration**: Steps 2-4 are repeated set number of times or until desired vocab is reached.
