# Leveraging Online Reviews for Evaluating Business Performance
This project presents a comprehensive framework for analyzing and predicting business
performance through customer reviews and combines rule-based methods, large language
models (LLMs), supervised and unsupervised learning, and a recommendation system. We
began with a comparative analysis of rule-based sentiment analysis tools to classify review
sentiment, which included VADER and TextBlob, and found that they were inconsistent
when tested against a gold standard set of 30 manually annotated reviews. We then moved
to a transformer-based model called bart-large-mnli and used its zero-shot sentiment classi-
fication ability, which resulted in performance improvement, but it failed to label “Neutral”
reviews appropriately. To improve reliability, we then used the ChatGPT API, particularly
GPT 4o, to label the reviews, which proved to be more consistent when tested on the gold
standard.
We calculated year-over-year deltas (2018-2019 and 2019-2020) for sentiment score and
other metrics of business engagement, and used them to train the XGBoost classifier that
predicts whether business engagement in 2021 increased, decreased, or remained stable. The
model achieved an accuracy of 74% and macro F1-score of 0.58 on the test set, with strong
precision on stable businesses and moderate performance on minority classes.
In parallel, a K-Means clustering model grouped businesses based on sentiment, average
rating, and review volume, showing distinct segments of participation. A 3-D visualization
and spatial mapping across California further illustrated regional patterns. Finally, we built a
location-aware recommendation system using KNN and cosine similarity, combining TF-IDF
review vectors, metadata, and sentiment. The system identifies similar businesses within a
specified radius and provides actionable improvement based on POS-tagged key differences.
Our results indicate that the techniques we have used and applied throughout the project
show promising results in evaluating business performance over a wide array of parameters,
including customer sentiment, which can give businesses significant leverage in understanding
customer experience and making data-driven strategic decisions for sustained engagement
and growth.
