# Unsupervised_ML_Clustering_with_K-means

Moosic's Automated Playlist Creation Project
Background: Moosic, a start-up creating curated playlists, is scaling up fast. To streamline playlist creation, they’re leveraging Data Science. Using a dataset with audio features collected from the Spotify API, the mission is to automate playlist creation using a clustering algorithm such as K-Means.

In this context, I'm dealing with songs that don’t have pre-defined labels or categories—we only have their audio features. By using K-Means clustering, we’re essentially letting the algorithm group similar songs together based on those features, without any prior knowledge of genres or playlists. It’s about discovery rather than instruction: the algorithm is figuring out the clusters on its own rather than being told what to look for.

**Steps Taken:**

**Data Collection:**

Dataset: Audio features (tempo, energy, danceability, etc.) collected from the Spotify API.

**Data Preparation:**

Normalization: Scaling audio features using MinMaxScaler for uniform data distribution.

Genre Definitions: Defining 25 genres based on audio features, ensuring diverse categorization.

**Clustering:**

Algorithm: K-Means used to cluster songs into playlists.

Cluster Assignment: Songs divided into clusters based on similar audio features.

**Genre and Playlist Assignment:**

Genre Assignment: Each song assigned a genre based on defined criteria.

Playlist Assignment: Each genre linked to a specific playlist.

Outcome: An initial prototype divides the dataset into clusters (playlists), assigning genres and linking them to specific playlists.

**Discussion Points:**

**Feature Effectiveness:**

Are Spotify’s audio features able to capture similarities between songs as humans do?

Can you identify two rock ballads, operas, or drum & bass songs using these features?

**Algorithm Efficiency:**

Is K-Means an effective method for creating playlists?

Would you consider sticking with K-Means or exploring other clustering algorithms for better accuracy?

**Outcomes:**

**K-means Clustering**: Using the K-means algorithm with a low number of clusters, such as 6, results in clusters that are not particularly cohesive.

![image](https://github.com/user-attachments/assets/92ebee38-8e92-46ed-b8b7-4fa1bcf2bd6f)

**Increasing Clusters**: Increasing the number of clusters to 25 improves the chances of forming more cohesive clusters, albeit somewhat randomly.


![image](https://github.com/user-attachments/assets/55b09456-08ec-4d42-8a71-c4c93dcfe34a)

**Spotify API**: A more effective approach for creating clusters is by using the Spotify API to group songs by genres.

![image](https://github.com/user-attachments/assets/b2b97aef-44b2-44de-b27b-ab8c1c791c5d)



