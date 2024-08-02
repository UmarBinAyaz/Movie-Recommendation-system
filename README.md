**Movie Recommendation System**

**Overview**

This project is a Movie Recommendation System that leverages machine learning techniques to suggest movies based on user preferences. 
By analyzing a dataset of movies and credits, the system can recommend similar movies to the one selected by the user. 
The front-end interface is built using Streamlit, providing an interactive and user-friendly experience.

**Features**

Content-Based Filtering: 
Uses movie metadata (tags) to recommend similar movies.

Cosine Similarity:
Calculates the similarity between movies based on their feature vectors.
Interactive UI: 
Built with Streamlit for a responsive and engaging user experience.

Poster Fetching: 
Integrates with The Movie Database (TMDb) API to fetch and display movie posters.


**Datasets**

The project utilizes two main datasets:

Movies Dataset: 
Contains information about movies.

Credits Dataset: 
Contains information about the cast and crew of the movies.

**Machine Learning Algorithms**

CountVectorizer: Converts text data into numerical feature vectors.

Cosine Similarity: Measures the similarity between movies based on their feature vectors.
