

## YouTube Comment Analysis Using NLP 

In this project, I worked on analyzing YouTube video comments using Natural Language Processing (NLP) techniques. The main goal was to extract and clean comments, detect spam, perform sentiment analysis, and visualize key insights.  

### Setting Up the Environment 

I started by importing essential libraries like `pandas`, `matplotlib`, `seaborn`, and `nltk`. Since I needed to process text data, I also included `wordcloud` for visualization and `SentimentIntensityAnalyzer` from `nltk` to analyze comment sentiments. Before running the code, I downloaded necessary NLTK resources, including stopwords and the VADER lexicon.  

### Fetching YouTube Data  

To get video data, I used the YouTube Data API. I created a dictionary of categories like Education, Gaming, News, Entertainment, and Technology, each containing relevant keywords. Using the API, I searched for videos related to these keywords, extracted details like video titles, descriptions, and channels, and stored them in a DataFrame.  

Next, I fetched the top comments for each video. Some videos had comments disabled, so I handled such cases by returning an empty list instead of breaking the script.  

### Cleaning and Filtering Comments

Raw YouTube comments often contain spam, special characters, and unnecessary words. To clean them, I:  
- Removed HTML tags and special characters.  
- Converted text to lowercase.  
- Removed common stopwords (like the, and, is).  
- Applied lemmatization to convert words to their base forms.  
- Implemented a spam filter by checking for keywords like *subscribe, check out, free money.  

### Visualizing Category Distribution  

Once I had cleaned the data, I plotted a bar chart to visualize the distribution of videos across categories. This helped in understanding how well different topics were represented in the dataset.  

### Word Frequency Analysis 

To identify the most commonly used words in YouTube comments, I merged all comments into a single text and created a frequency count. I then plotted the top 10 most frequent words using a bar chart.  

Additionally, I generated a word cloud, which visually represents the most common words, making it easier to spot recurring themes in YouTube discussions.  

### Sentiment Analysis

For sentiment classification, I used VADER from `nltk`, which is well-suited for analyzing short social media texts. I assigned comments a Positive, Negative, or Neutral label based on their sentiment scores. The sentiment distribution was then plotted as a pie chart, giving an overview of whether most comments were positive or negative.  

### Conclusion 

This project helped me explore YouTube comments from a data science perspective. I was able to:  
- Automate the process of fetching and analyzing YouTube data.  
- Filter out spam and clean noisy text data.  
- Identify popular discussion topics.  
- Perform sentiment analysis to understand audience reactions.  

Going forward, I can refine this by incorporating deep learning models for sentiment analysis, improving spam detection, or even developing a real-time YouTube comment analyzer.
