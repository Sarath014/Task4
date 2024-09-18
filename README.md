from textblob import TextBlob
import matplotlib.pyplot as plt

# Define a list of tweets
tweets = ["I love this product!", "This product is terrible.", "I'm neutral about this product."]

# Analyze sentiment for each tweet
sentiments = [TextBlob(tweet).sentiment.polarity for tweet in tweets]

# Visualize sentiment distribution
plt.hist(sentiments, bins=50)
plt.xlabel('Sentiment Score')
plt.ylabel('Frequency')
plt.title('Sentiment Distribution')
plt.show()
