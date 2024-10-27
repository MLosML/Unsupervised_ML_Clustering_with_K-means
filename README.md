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
![image](https://github.com/user-attachments/assets/a9a33631-1e40-4a73-bde2-61472eb8cc70)


Outcome: An initial prototype divides the dataset into clusters (playlists), assigning genres and linking them to specific playlists.

Discussion Points:

Feature Effectiveness:

Are Spotify’s audio features able to capture similarities between songs as humans do?

Can you identify two rock ballads, operas, or drum & bass songs using these features?

Algorithm Efficiency:

Is K-Means an effective method for creating playlists?

Would you consider sticking with K-Means or exploring other clustering algorithms for better accuracy?
