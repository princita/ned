<code>
pip install nltk
import nltk
</code>

# Download required resources
<code>
nltk.download('punkt')
nltk.download('omw-1.4')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
</code>
<code>
from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer()
</code>
<code>
word = "running"
lemma = lemmatizer.lemmatize(word, pos='v')  # 'v' indicates it is a verb
print(lemma)  # Output: run
</code>

<code>  
from nltk.tokenize import word_tokenize, sent_tokenize
text = "NLTK is a powerful library for natural language processing tasks."
tokens = word_tokenize(text)
print(tokens)  # Output: ['NLTK', 'is', 'a', 'powerful', 'library', 'for', 'natural', 'language', 'processing', 'tasks', '.']
sentences = sent_tokenize(text)
print(sentences)  # Output: ['NLTK is a powerful library for natural language processing tasks.']
from nltk.stem import PorterStemmer
stemmer = PorterStemmer()
word = "running"
stem = stemmer.stem(word)
print(stem)  # Output: run
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize
</code>

# Download the stop words corpus
<code>
nltk.download('stopwords')

text = "NLTK is a powerful library for natural language processing tasks."
</code>

# Tokenize the text
<code>
tokens = word_tokenize(text)
</code>
# Get the English stop words
<code>
stop_words = set(stopwords.words('english'))
</code>

# Filter out the stop words
<code>
filtered_tokens = [word for word in tokens if word.casefold() not in stop_words]
print(filtered_tokens)
</code>
