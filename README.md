## Introduction
This project involves predicting the popularity of Spotify songs based on various features using machine learning models.

## Libraries and Environment
The project is implemented in Python using Jupyter Notebook.
It utilizes libraries such as Scikit-learn, Keras, Pandas, and others for various tasks including data manipulation, visualization, natural language processing, and model training.
The environment is set up using Google Colab with specific directory configurations.

## Data Preparation
### Datasets
#### 30,000 Spotify Songs (kaggle.com)
https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs?resource=download
A dataset of 23 columns containing data on:
- Track ID
- Track Name
- Artist
- Popularity
- Album ID
- Album Name
- Album Release Date
- Playlist Name
- Playlist ID
- Playlist Genre
- Playlist Subgenre
- Danceability
- Energy
- Key
- Loudness
- Mode
- Speechiness
- Acousticness
- Instrumentalness
- Liveness
- Valence
The data was collected from the Spotify platform and primarily focuses on the most popular commercial songs.
#### Music Artists Popularity (kaggle.com)
https://www.kaggle.com/datasets/pieca111/music-artists-popularity
A dataset of 10 columns containing data on:
- MusicBrainz ID
- Artist Name (MusicBrainz)
- Artist Name (Last.fm)
- Country (MusicBrainz)
- Country (Last.fm)
- Tags (MusicBrainz)
- Tags (Last.fm)
- Last.fm Listeners
- Last.fm Scrobbles
- Ambiguous Artist
The data was obtained from Last.fm and MusicBrainz platforms and mainly concerns popular commercial songs.

### Data Reliability Assessment
The reliability of both datasets is considered high because the data consists of publicly available information retrieved from Spotify and Last.fm platforms, and the mathematical data was obtained through calculations. The datasets do not include opinions, comments, or subjective information.

### Usage
These datasets contain a wide range of information about songs, playlists, and popularity ratings. They can be used to train models that predict the popularity of new songs based on their characteristics. Additionally, feature importance analysis can be conducted to determine which characteristics (e.g., estimated "loudness" impact on popularity) are most significant.

### Joining Datasets
The datasets are merged to combine artist and song information.

## Model Training
### Splitting Data
The data is split into training and test sets using an 80/20 split ratio.

### Model Types
#### Ridge Regression (Linear Model)
Utilizes RidgeCV from Scikit-learn. Score: 0.25
### SVR - deprecated
The model was tested and abandoned due to very long training time and low score.
#### K-Nearest Neighbors (KNN)
GridSearchCV is employed to optimize the number of neighbors. Score: 0.60
#### Random Forest
Trains a RandomForestRegressor with specified hyperparameters. Score: 0.60
#### Gradient Boosting (Best Performing Model)
Trains a GradientBoostingRegressor with a specific set of hyperparameters. This is best-performing model with optimal time and score which was saved and intended for further development of the project. Score: 0.72
#### Neural Network
Implements a Sequential neural network using Keras with various configurations of dense layers. Score: 0.53

### Model Evaluation
Each trained model's performance is evaluated using R-squared scores on both training and test datasets.

## Results and Visualization
The project includes visualizations such as KDE plots and regression plots to visualize the predicted vs. actual popularity scores.

## Conclusion
This project showcases the use of different machine learning techniques to predict song popularity based on Spotify features. The best-performing model is the Gradient Boosting Regressor.
