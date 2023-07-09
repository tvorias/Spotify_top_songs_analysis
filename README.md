# Spotify_top_songs_analysis

## Use case
The script applies several statistical computations to analyze the top 10,000 songs streamed on Spotify and visualizes the findings. The script utilizes two sources of data: a publically-available Kaggle dataset of Spotify's top 10,000 streamed songs and data sourced using Spotipy, which is a Python library for the Spotify Web API. Computations include (1) a linear regression model to predict a song's total streams based on number of days since the song's release, how high it made it up in the charts, how many times it made the top 10, and audio features, including acousticness, energy, speechiness, loudness, valence, instrumentalness, liveness, and danceability; (2) an agglomerative clustering model to identify similarities between the top 500 songs; (3) a decision tree classifier and neural network classifier to predict if a song would make it into the top 10 at any given point in time based on its total streams and audio features. 

# Set up
### Dependencies
- `Python3`
- `Spotify_final_dataset.csv`
  - Kaggle dataset available [here](https://www.kaggle.com/datasets/rakkesharv/spotify-top-10000-streamed-songs)
- Spotipy Client Credentials
  - To access a client id and client secret key, you will need to create an app with Spotipy. Once you register your app, you will receive your client id and secret key. Instructions can be found [here](https://spotipy.readthedocs.io/en/2.6.3/#getting-started)
 
### Installations
Prior to running the program, you will need to run the following installations:

 - `!pip install seaborn`
 - `!pip install spotipy`
 - `!pip install --default-timeout=100 future`

These installations are already written in the imports code block for your convenience. 

## Running the script
- First, you will need to download the `Spotify_final_dataset.csv` file. Next, run the first code block to perform the necessary pip installs and imports.
- Once you've obtained both the client id and secret key, replace `apiInfo['client_id']` and  `apiInfo['client_secret']` in the code with your personal client id and secert key.
- From there, the script can be run. Results will be printed below each code block. 
