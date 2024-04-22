- tweets = [
    "I'm so worried about the spread of coronavirus. It's getting out of control!",
    "Feeling hopeful that the vaccine rollout will help bring an end to the pandemic.",
    "Coronavirus lockdown has been tough, but we're all in this together!",
    "The government's response to coronavirus has been disappointing. They need to do better.",
    "Just tested positive for COVID-19. Feeling scared and isolated."
]

# Perform sentiment analysis on tweets
for tweet in tweets:
    # Analyze sentiment
    analysis = TextBlob(tweet)
    sentiment = analysis.sentiment

    # Determine sentiment label
    if sentiment.polarity > 0:
        sentiment_label = 'Positive'
    elif sentiment.polarity < 0:
        sentiment_label = 'Negative'
    else:
        sentiment_label = 'Neutral'

    # Print tweet and sentiment analysis result
    print("Tweet:", tweet)
    print("Sentiment:", sentiment_label)
    print()



