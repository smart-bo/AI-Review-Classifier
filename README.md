# AI Review classifier
 A practice of AI NLP model build, train and test. 
### Overview
Scrape source datasets from IMDB and create Naïve Bays Classifier model to classify test review to positive or negative. Calculate correctness rate of the result at the end.   (Datasets: first 5 seasons of series 'Friends'.)
### Libraries
- **Beautifulsoup**  (scrape reviews)
- **Pandas**  (output format, probability)
- **Textblob**  (tokenize words)
- **Math**  (calculate log )
- **Matplotlib**  (draw graph)
### Processes
- Extract reviews from IMDB, save in `data.csv`. Consider the review which user’s score greater than or equal to 8.0 as a positive review, otherwise, it is a negative one. The program read all the review contents under the link of Review Link page, consider all the reviews on the first page, not for the “Load More” button.
- Fold the Reviews to lowercase and tokenize the words as vocabulary. For each word wi in the training dataset, compute its frequency and its conditional probability. These probabilities must be smoothed with 𝛿 = 1. 
- All the words that are removed from the vocabulary are saved in `remove.txt`. 
- Save the results in the text file named `model.txt`.
- Use Naïve Bays Classifier to classify the testing dataset. To avoid arithmetic underflow, work in `log10` space. The results of classified reviews are saved in `result.txt`.
- Calculate the correctness rate of the model at the end of `result.txt` file.
- Gradually change the smoothing value from 𝛿 = 1 to 𝛿 = 2 in steps of 0.2. Save the results of 𝛿 = 1.6 in `smooth-model.txt` and `smooth-result.txt`.
- Plot the performance of the classifiers (correctness of prediction) for different smoothing values against different smoothing values as a graph.
### References
https://www.imdb.com/title/tt0108778/

