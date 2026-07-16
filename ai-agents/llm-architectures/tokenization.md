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
