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

### libraries and documents required to run Writing Style Analysis
1. [Natural Language Toolkit](https://www.nltk.org/install.html)
- NLTK is a suite of libraries and programs for symbolic and statistical natural language processing. 
```
pip install nltk
```

2. [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#installing-beautiful-soup)
- Beautiful Soup is a Python library for pulling data out of HTML and XML files. It is used to web scrape the posts from the various URLs.
```
pip install beautifulsoup4
```

3. [numpy](https://numpy.org/install/)
- numpy is a Python library which supports a large collection of high-level mathematical functions. It is used to perform simple average functions in this assignment.
```
pip install numpy
```

4. [requests](https://docs.python-requests.org/en/latest/user/install//)
- requests is a simple, yet elegant, HTTP library. It is used to read posts' text from URLs in this assignment.
```
pip install requests
```

5. [docx2text](https://pypi.org/project/docx2txt/#history)
- docx2text is a pure python-based utility to extract text and images from docx files. It used to read text from URLs with web scraping blocked (CNA posts) from a word document in this assignment. 
```
pip install docx2text
```

6. [language_tool_python](https://pypi.org/project/language-tool-python/)
- language_tool_python checks grammar using LanguageTool. It is used to perform grammar checks on the text in this assignment.
```
pip install language-tool-python
```

7. CNA Post Documents
- 2 Word Documents (cnaOne and cnaTwo) contain the posts from 2 URLs from CNA. Web scraping had been blocked for CNA which resulted manually storing the posts in word documents to be read from the program during execution. 


### Results 
#### 3.4 Application 

**Input text: "I ordered this chair last week. The condition was really good. The support is comfortable for the back and the seat is strong"**

LIME output:
![Positive Prediction](pos_pred.png)

**Input text: "Never again! The service was so slow and the food was not good."**

LIME output:
![Negative Prediction](neg_pred.png)

Using the LIME tool we are able to identify the probability of contribution to a specific label for every token in the text. From the 2 sample predictions above we can see that the model is more confident in making positive predictions as the dataset is biased towards positive reviews. Although words like 'Never' or 'Not' are used one positive word 'good' contributes highly towards the final prediction of the negative review. 


