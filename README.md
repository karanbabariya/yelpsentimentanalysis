# yelpsentimentanalysis
Scraped over 5000 reviews and star ratings of various Toronto restaurants as training data for a simple Naive Bayes classifier to do sentiment analysis into two positive and negative classes by using Yelp Fusion API

Web Scraping
Scraped the content from the business URLs obtained from the Yelp Fusion's business API. Once the URLs are obtained, iterate through all the restaurants' response objects to fetch reviews and star ratings. The limit of 50 restaurants and 100 reviews per restaurant is kept to prevent overloading of public website. A total of 5000 reviews has been fetched.

Data preparation
Once the reviews are fetched, the data is split into positive and negative reviews based on user's star ratings. If star rating is > 3 then review is positive, otherwise it is termed negative. Fetched data had 4205 positive reviews and just 795 negative reviews. In order to address imbalance of the dataset, oversampling of negative reviews is done. Review count now increases to 8410.

Bayes Classifier
Data is now split into training and validation dataset. Using Sentiment Analyzer, naive bayes classifier is trainied. This trained model is used on validation dataset which gave an accuracy of 78.87% with an F-measure [negative]: 76.81268882175226 and F-measure [positive]: 80.59418457648546.

Model can further be improved by using more data.
