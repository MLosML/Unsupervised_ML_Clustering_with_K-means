# Unsupervised_ML_Clustering_with_K-means

Moosic's Automated Playlist Creation Project
Background: Moosic, a start-up creating curated playlists, is scaling up fast. To streamline playlist creation, they’re leveraging Data Science. Using a dataset with audio features collected from the Spotify API, your mission is to automate playlist creation using a clustering algorithm such as K-Means.

Steps Taken:

Data Collection:

Dataset: Audio features (tempo, energy, danceability, etc.) collected from the Spotify API.

Data Preparation:

Normalization: Scaling audio features using MinMaxScaler for uniform data distribution.

Genre Definitions: Defining 25 genres based on audio features, ensuring diverse categorization.

Clustering:

Algorithm: K-Means used to cluster songs into playlists.

Cluster Assignment: Songs divided into clusters based on similar audio features.

Genre and Playlist Assignment:

Genre Assignment: Each song assigned a genre based on defined criteria.

Playlist Assignment: Each genre linked to a specific playlist.

Key Code Snippets:
import pandas as pd

# Define genres and playlists
genres = {'Pop': {'danceability': 0.7, 'energy': 0.6}, 'Rock': {'loudness': -12, 'energy': 0.7}, ... 'Other': {}}
playlists = {'Pop': 'Pop Playlist', 'Rock': 'Rock Playlist', ... 'Other': 'Other Playlist'}

# Function to assign genres based on features
def assign_genre(row):
    for genre, criteria in genres.items():
        if all(row[feature] > threshold for feature, threshold in criteria.items()):
            return genre
    return 'Other'

# Function to assign playlist based on genre
def assign_playlist(row):
    return playlists.get(row['genre'], 'Other Playlist')

# Applying the functions
songs_scaled_min_max['genre'] = songs_scaled_min_max.apply(assign_genre, axis=1)
songs_scaled_min_max['playlist'] = songs_scaled_min_max.apply(assign_playlist, axis=1)

Outcome: An initial prototype divides the dataset into clusters (playlists), assigning genres and linking them to specific playlists.

Discussion Points:

Feature Effectiveness:

Are Spotify’s audio features able to capture similarities between songs as humans do?

Can you identify two rock ballads, operas, or drum & bass songs using these features?

Algorithm Efficiency:

Is K-Means an effective method for creating playlists?

Would you consider sticking with K-Means or exploring other clustering algorithms for better accuracy?
