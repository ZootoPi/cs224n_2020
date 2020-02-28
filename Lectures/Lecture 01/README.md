# Introduction and Word Vectors

- [Slide](http://web.stanford.edu/class/cs224n/slides/cs224n-2020-lecture01-wordvecs1.pdf)
- [Note](http://web.stanford.edu/class/cs224n/readings/cs224n-2019-notes01-wordvecs1.pdf)
- Suggested Readings:
    1. [Word2Vec Tutorial - The Skip-Gram Model](http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/)
    2. [Efficient Estimation of Word Representations in Vector Space](http://arxiv.org/pdf/1301.3781.pdf)
    3. [Distributed Representations of Words and Phrases and their Compositionality](http://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)


# Keynote
- A word is a __signifier__ that maps to a __signified__ (idea or thing).
- Word representation:
    - As discrete symbol:
        - __One-hot encoding__: 
            - Represent words by one-hot vectors.
            - Cons:
                - Vector dimension = number of words in vocabulary.
                - No natural notion of similarity.
    - By the context:
        - “You shall know a word by the company it keeps” (J. R. Firth 1957: 11)
        - Distributed representation:  Word vectors = word embeddings =  word representations. 
        - __SVD based method__: Use SVD to reduce vector dimension.
            - ___Word document matrix___: focus on hidden topic (i.e LSA).
            - ___Window based co-occurence matrix___: focus on semantic and syntactic part.
            - Cons:
                - The dimensions of the matrix change very often.
                - Extremely sparse and very high dimensional matrix in general.
                - Quadratic cost to train ...
            - Solution:
                - Ignore stopwords
                - Apply a ramp window 
                - Use Pearson correlation and set negative counts ...
        - __Iteration based method__:   
            - Language models:
            - __Word2vec__:
                - 2 algorithms: 
                    - Continuous bag-of-words (CBOW).
                    - Skip-gram.
                - 2 training methods: 
                    - Negative sampling.
                    - Hierarchical softmax.

