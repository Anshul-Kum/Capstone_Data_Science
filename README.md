# Leveraging Online Reviews for Evaluating Business Performance
This project introduces a robust framework for analyzing and predicting business performance using customer reviews. We combined various AI techniques, including rule-based methods, large language models (LLMs), and both supervised and unsupervised learning.

Our approach involved:

Sentiment Analysis Refinement: We initially explored rule-based sentiment tools (VADER, TextBlob) but found inconsistencies. We then experimented with zero-shot classification using bart-large-mnli, which showed improvement but struggled with "Neutral" reviews. Ultimately, we leveraged the ChatGPT API (GPT-4o) to accurately label review sentiment, significantly enhancing reliability.

Engagement Prediction: We calculated year-over-year changes (deltas) in sentiment scores and other business engagement metrics. These features were used to train an XGBoost classifier that predicts whether business engagement will increase, decrease, or remain stable. The model achieved 74% accuracy and a macro F1-score of 0.58, showing strong performance for stable businesses.

Business Segmentation: A K-Means clustering model was developed to group businesses based on sentiment, average rating, and review volume, revealing distinct customer participation segments. These segments were visualized in 3D and mapped spatially across California to highlight regional patterns.

Location-Aware Recommendation System: We built a recommendation system using K-Nearest Neighbors (KNN) and cosine similarity. This system combines TF-IDF review vectors, business metadata, and sentiment to identify similar businesses within a specified radius. It also offers actionable improvement suggestions by highlighting key differences identified through POS-tagging.
