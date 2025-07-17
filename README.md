# Project – Cyberbullying and Non-Bullying Tweets: Network Analysis

This project examines the structural and topical characteristics of cyberbullying and non-bullying tweets by constructing and analyzing two types of networks.

## Network Types

### Network Type 1 – Tweets as Nodes
- **Node definition**: Each node represents a tweet.
- **Vectorization**: Tweets were vectorized using `TfidfVectorizer` from scikit-learn.
- **Edge definition**: Cosine similarity between tweets' TF-IDF vectors.
- **Filtering**: Edges with cosine similarity below 0.6 were removed.

### Network Type 2 – Words of Post as Nodes
- **Node definition**: Each node represents a word.
- **Vectorization**: Words were vectorized using fastText embeddings.
- **Edge definition**: Cosine similarity between word vectors.
- **Filtering**: Same similarity threshold and stopwords/URLs removed.

## Research Questions

1. What are the central and influential topics and keywords of bullying and non-bullying tweets?
2. Is there a difference in the diversity of topics in bullying and non-bullying tweets?

## Analysis Techniques

### Network Type 1
- **Centrality Measures**: Degree Centrality, PageRank, Closeness Centrality.
- **Community Detection**: Louvain method and modularity score.
- **Topic Exploration**: Manual interpretation and comparison of influential tweets and communities.

### Network Type 2
- **Diversity Measure**: Number of connected components in each tweet-based word network.
- **Comparison**: Average number of connected components across bullying and non-bullying samples.

## Key Findings

- **Influential Topics**: Bullying tweets commonly centered around racism and public figures (e.g., Miley Cyrus). Non-bullying tweets discussed reality TV, wellness, and politics.
- **Community Structure**: Many tweet communities consisted of slightly altered versions of the same post. Modularity score was similar for both networks.
- **Topic Diversity**: The number of connected components was slightly higher in non-bullying tweets, suggesting marginally greater diversity.

## Limitations

- The classification source of tweets was unclear.
- Many tweets were near duplicates.
- Manual interpretation of tweet communities is prone to bias.
- Small dataset size (≈100 tweets per network after filtering).

## Files Included

- `Project Report.pdf`: Full report with analysis, methodology, visualizations, and conclusions.
- `data/cyberbullying_tweets.csv`: Raw or cleaned dataset used for the analysis.

## Suggested Future Work

- Analyze data from other platforms (Reddit, Instagram).
- Improve filtering of similar tweets prior to network construction.
- Focus on hashtags or other metadata for topic clustering.

