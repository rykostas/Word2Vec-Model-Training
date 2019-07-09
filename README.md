## Training Word2Vec Model on English Wikidumps using Gensim
# Vector Space Model
Words have semantically different meanings in daily use except lexicon meanings, and these semantic meanings depends on a text. In publication of "[Distributional Structure](https://www.tandfonline.com/doi/abs/10.1080/00437956.1954.11659520)", Harris [1] advocates that if two different words are elements of a group that has semantically close, these two words can be said to be similar.
Vector space model (in another saying distributional model) represents a system that creates word vectors from given corpus based on an unsupervised model. All words in a context represent with a dot and semantically related words tend to be close together in this space. 

# Word2Vec Model
Word2vec is used for learning vector representations of words.This prediction-based method called Word2vec, developed by Mikolov et al [2], uses a neural network to perform a fruitful vector representation of unstructured text data.  Look at Mikolov and colleagues articles regarding Word2vec representation; [Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/pdf/1301.3781.pdf), [Distributed Representations of Words and Phrases and their Compositionality](https://arxiv.org/abs/1310.4546).

# Word2Vec Model by Gensim
Gensim provides Word2vec model training tool to create easily model file. [In here](https://radimrehurek.com/gensim/models/word2vec.html), you can look at this module in detailed.
When creating the model, the data should be provided as list of list. This type of list is an ordered collection of values, where each value is in turn a list. There are some parametres to build a model. The main parametres are;
* `size (int, optional)` # Dimensionality of the word vectors.
* `window (int, optional)`             # Maximum distance between the current and predicted word within a sentence. 
* `sg ({0, 1}`             # Training algorithm: 1 for skip-gram, 0 for CBOW. 

In our work we try different dimensions and window sizes, also trained with Skip-Gram and Continuous Bag Of Words (CBOW) algorithms.Differences between two algorithms you can look at [here](https://towardsdatascience.com/word2vec-skip-gram-model-part-1-intuition-78614e4d6e0b)


# References
[1] Z. S. Harris, “Distributional structure,” Word, vol. 10, no. 2-3, pp. 146-162, 1954.

[2] T. Mikolov, I. Sutskever, K. Chen, G. S. Corrado and J. Dean, “Distributed representations of words and phrases and their compositionality,” in Advances in neural information processing systems, 2013.
