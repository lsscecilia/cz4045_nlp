### CZ4045 Natural Language Processing
## Assignment 1

### List of 3rd-party open source packages
1. [LIME](https://github.com/marcotcr/lime)
- LIME is an Explainable AI open source package used to explain reasonings behind model predictions. 
2. VADER
```
nltk.download('vader_lexicon')
from nltk.sentiment.vader import SentimentIntensityAnalyzer
```
3. [tqdm](https://pypi.org/project/tqdm/)
- tqdm is used to track progress of loading GloVe vectors in the application portion of the assignment
```
pip install tqdm
```
4. [GloVe embedded vector](https://nlp.stanford.edu/projects/glove/) 
- Download the glove6B.zip file from the link above 
- Extract the *glove.6B.100d.txt* to be used for the code in 3.4 Application


### Results 
#### 3.4 Application 

**Input text: "I ordered this chair last week. The condition was really good. The support is comfortable for the back and the seat is strong"**

LIME output:
![Positive Prediction](pos_pred.png)

**Input text: "Never again! The service was so slow and the food was not good."**

LIME output:
![Negative Prediction](neg_pred.png)

Using the LIME tool we are able to identify the probability of contribution to a specific label for every token in the text. From the 2 sample predictions above we can see that the model is more confident in making positive predictions as the dataset is biased towards positive reviews. Although words like 'Never' or 'Not' are used one positive word 'good' contributes highly towards the final prediction of the negative review. 


### libraries required to run POS tagging
1. [Natural Language Toolkit](https://www.nltk.org/install.html)
- NLTK is a suite of libraries and programs for symbolic and statistical natural language processing. It is used as one of the two toolkits for pos tagging.
```
pip install nltk
```

2. [spaCy](https://spacy.io/usage)
- spaCy is an open-source software library for advanced natural language processing. It is used as one of the two toolkits for pos tagging.
```
pip install spacy
python -m spacy download en_core_web_sm
```

2. [pandas](https://pandas.pydata.org/docs/getting_started/install.html)
- pandas is a Python package that provides fast, flexible, and expressive data structures, used in this assignment to display the results obtained.
```
pip install pandas
```
