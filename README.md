# Movie Recommendation System

## Overview
This project is a **Movie Recommendation System** that leverages machine learning techniques to suggest movies based on user preferences. By analyzing a dataset of movies and credits, the system can recommend similar movies to the one selected by the user. The front-end interface is built using **Streamlit**, providing an interactive and user-friendly experience.

## Features
- **Content-Based Filtering**: Uses movie metadata (tags) to recommend similar movies.
- **Cosine Similarity**: Calculates the similarity between movies based on their feature vectors.
- **Interactive UI**: Built with Streamlit for a responsive and engaging user experience.
- **Poster Fetching**: Integrates with The Movie Database (TMDb) API to fetch and display movie posters.

## Datasets
The project utilizes two main datasets:
1. **Movies Dataset**: Contains information about movies.
2. **Credits Dataset**: Contains information about the cast and crew of the movies.

## Machine Learning Algorithms
- **CountVectorizer**: Converts text data into numerical feature vectors.
- **Cosine Similarity**: Measures the similarity between movies based on their feature vectors.

## Implementation

### Data Preparation
```python
import pandas as pd
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.metrics.pairwise import cosine_similarity

movies = pd.read_csv('tmdb_5000_movies.csv')
credits = pd.read_csv('tmdb_5000_credits.csv')

cv = CountVectorizer(max_features=5000, stop_words='english')
vectors = cv.fit_transform(new_df['tags']).toarray()

similarity = cosine_similarity(vectors)

def recommend(movie):
    movie_index = new_df[new_df['title'] == movie].index[0]
    distances = similarity[movie_index]
    movies_list = sorted(list(enumerate(distances)), reverse=True, key=lambda x: x[1])[1:6]

    for i in movies_list:
        print(new_df.iloc[i[0]].title)
    return
