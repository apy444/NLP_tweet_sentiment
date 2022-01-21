internet_archive_filter.ipynb
reads global sample of tweets from s3 and filter the data to keep only tweets relevant to S&P 500 companies.

merge.ipynb
merge tweets obtained internet_archive_filter.ipynb notebook with financial tweet data from kaggle data set. Additionally enrich kaggle dataset with company industry and normalize date format.

aggregate.ipynb
counts positive/negative tweets per day per company (to be used for the UI).

stock_model_more_efficient.ipynb
extracts features from the final financial tweets dataset by using TF-IDF technique and lexicon based approach. Additionally pre processes the data so as to remove stop words, URLs and hashtags from tweets.
trains a Naive Bayes classififier model trained on labeled (sentiment) tweets, and predicts financial dataset sentiment for each tweet.

recommend_influencers.ipynb
combine tweets with sentiment scoring and financial information.Returns which Twitter accounts had a best correlation with stock movements; i.e. which accounts had tweets with positive sentiment on days that the stock price went up, and negative sentiment on days that the stock price went down.

merge_financial_w_sentiment.ipynb
merges the financial data with tweet sentiment data to be used for the UI.

emoticons_as_features.ipynb
contains function that creates additional emoticon based features, and counts the documents that contain emoticons (due its very low ratio this feature was not used in the model)

correlation.ipynb
calculates the correlation between tweet sentiment and stock price movements, for each company
