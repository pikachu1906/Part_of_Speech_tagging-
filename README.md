# Part_of_Speech_tagging

### _Assumptions_:   

- The image contains sentences and words in English.
- The typeface used in the image is the same fixed-width and size. For example, each letter is contained in a box that is 25 pixels height by 16 pixels wide.
- Another presumption we make is that we only take into account the Latin alphabet's 26 capital, 26 lowercase, 10 numerals, spaces, and 7 punctuation-symbol symbols.
- The image's I/O is handled by the skeleton code, which turns the image into a list of lists that represents a two-by-two grid of black and white dots.  

### _Approach_:   

- We have determined the character-to-character transition probabilities for this problem, exactly like we did for the word-to-word transition probabilities in the prior problem.  

### _Simplified Bayes Net_:   
- In this method, we obtain the character with the highest probability using the emission probability. We then join that character to the remainder of the string and output it.  

### _Viterbi-Hidden Markov Models_:  
- For the dynamic programming approach we are storing the probability values in a 2 column matrix   
- I first tested it as the ratio of the total number of pixels to the number of matched pixels. This was a total failure.  
Next approach was assigning categorical emission probabilities depending on level of correctness    
- Also normalized the probabilities for scaling purpose but only for emission probabilities as transition probabilities have very low value so scaled them up a bit in order to have higher contribution to the prediction than just emission probabilities     
- The final results were were correct enough by using this approach   
