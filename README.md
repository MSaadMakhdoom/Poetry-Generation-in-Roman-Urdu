# Poetry Generation in Roman Urdu

- Processing of urdu sentences. Use n-gram language modeling to generate some poetry using the spaCy pipeline for text processing.  
- The generational model can be trained on the provided poetry corpus containing poems from Faiz, Ghalib and Iqbal. 
- Scraping online sources (such as rekhta.org, hamariweb.com) to get a better representation of Urdu poetry.
- Train model in Urdu and convert the generated version into Roman using urdu to roman urdu translate. 
- Train bigram and trigram models using this corpus. Models used to generate poetry.
 
 ## Generate a ghazal using different models.
# Implementation of Algorithm: 
- Load the Poetry Corpus
- Tokenize the corpus in order to split it into a list of words
- Generate n-gram models
- For each of the stanzas
– For each verse
* Generate a random number in the range [6...8]
* Select first word (intelligently)
* Select subsequent words until end of verse
*  Try to rhyme the last words of the stanza with the last word of the first stanza
* Print verse
– Print empty line after stanza
## Implementation Challenges
- Solving selection of subsequent words . Predict the next word to compute is the most probable next word out of all of the possible next words. In other words, find the set of words that occur most frequently after the already selected word and pick the next word from that set. 
- Use a Conditional Frequency Distribution (CFD) to figure that out! A CFD tells us: given a condition, what is likelihood of each possible outcome.
## Standard n-gram Models
- Develop model using the Conditional Frequency Distribution method. First develop a Bigram model and then the Trigram model. Select the first word of each line randomly from starting words in the vocabulary and then use the bigram model to generate the next word until the verse is complete.
- Generate the next verse similarly. Follow the same steps for the trigram model and compare the results of the two n-gram models. 
## Backward Bigram Model
- Standard n-gram language models model the generation of text from left to right. However, in some cases, words might be better predicted from their right context rather than their left context. 



## Bidirectional Bigram Model
- BidirectionalBigramModel that combines the forward and backward model. Both the Back wardBigramModel and BidirectionalBigramModel should take the same input and produce the same style of output as BigramModel. Compare the output of the BidirectionalBigramModel with the Trigram model.
