<h1 align="center"> <a href="https://open.spotify.com" target="_blank"> <img src="https://github.com/mrankitgupta/Spotify-Data-Analysis-using-Python/blob/main/images/social-spotify.svg" alt="Spotify" width="55" height="40"/> </a> Spotify -  Music Recommendation System and Data Analysis  <a> </h1>


### About the Project

Spotify is a Swedish audio streaming and media services provider founded in April 2006. It is the world's largest music streaming service provider and has over 381 million monthly active users, which also includes 172 million paid subscribers.


![Spotify logo](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/26b5935a-85dc-4428-9038-39d6de77a5c0)


---

# Spotify Music Recommendation System

This project presents a Music Recommendation System built using the Spotify dataset. The system leverages advanced data analysis and machine learning techniques to recommend songs based on user preferences.


## Introduction

The Spotify Music Recommendation System aims to recommend songs that align with a user's listening history. By analyzing patterns in song popularity, audio attributes, and genres, the system can suggest songs that are similar to those the user already enjoys. This project highlights the power of data analysis and machine learning in creating personalized user experiences.

## Features

- **Data Extraction**: Uses Spotipy to fetch song data from the Spotify Web API.
- **Exploratory Data Analysis (EDA)**: Identifies key features and patterns in the Spotify dataset.
- **Feature Engineering**: Selects relevant features to build an accurate recommendation model.
- **Recommendation System**: Recommends songs based on user-input songs using cosine similarity.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/spotify-music-recommendation.git
   cd spotify-music-recommendation
   ```

2. **Install the required libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Spotify API credentials**:
   - Create an app on the [Spotify Developer's page](https://developer.spotify.com/).
   - Save your Client ID and Secret Key.
   - Set the environment variables:
     ```bash
     export SPOTIFY_CLIENT_ID='your_client_id'
     export SPOTIFY_CLIENT_SECRET='your_client_secret'
     ```

## Usage

1. **Import necessary libraries**:
   ```python
   import spotipy
   from spotipy.oauth2 import SpotifyClientCredentials
   import pandas as pd
   import numpy as np
   from collections import defaultdict
   from sklearn.metrics import euclidean_distances
   from scipy.spatial.distance import cdist
   import difflib
   import os
   ```

2. **Authenticate and initialize Spotipy**:
   ```python
   sp = spotipy.Spotify(auth_manager=SpotifyClientCredentials(client_id=os.environ["SPOTIFY_CLIENT_ID"],
                                                              client_secret=os.environ["SPOTIFY_CLIENT_SECRET"]))
   ```

3. **Define functions to fetch song data and calculate recommendations** (full code provided in the repository).

4. **Get song recommendations**:
   ```python
   recommended_songs = recommend_songs([
       {'name': 'Come As You Are', 'year': 1991},
       {'name': 'Smells Like Teen Spirit', 'year': 1991},
       {'name': 'Lithium', 'year': 1992},
       {'name': 'All Apologies', 'year': 1993},


---

## Objective

- **Leverage Spotify's Rich Dataset for Personalized Music Recommendations**: The primary objective of this project is to utilize the extensive dataset provided by Spotify to develop a sophisticated Music Recommendation System. By conducting an in-depth Exploratory Data Analysis (EDA), we aim to uncover patterns and relationships within the data that can be used to recommend songs tailored to individual user preferences. This involves identifying key audio features and metadata that influence music popularity and listener engagement.

## Music Recommendation System Explanation

- **Building a Data-Driven Music Recommendation Engine**: The Music Recommendation System is designed to suggest songs based on user input, leveraging advanced data analysis and machine learning techniques. By utilizing Spotipy, a Python client for the Spotify Web API, the system fetches detailed song data, including audio features and metadata. The system calculates the cosine similarity between the mean vector of user-input songs and other songs in the dataset, effectively identifying and recommending songs with similar audio characteristics and metadata. This approach ensures that the recommendations are highly relevant and personalized, reflecting the user's music taste and preferences.

---

## Exploratory data analysis (EDA) and Data Visualization

The project entails an engaging and insightful exploratory data analysis (EDA) and data visualization initiative, centered around the rich and extensive dataset sourced from Spotify. Powered by the versatile programming language Python and harnessed by statistical methodologies, this endeavor delves into uncovering the hidden gems within the realm of music streaming.

- The primary objective of this project revolves around distilling valuable insights from the vast musical catalog on Spotify. Utilizing a range of cutting-edge Python libraries, including Pandas for data manipulation, NumPy for numerical computations, Matplotlib for comprehensive data visualization, and Seaborn for enhancing the visual aesthetics, the project embarks on a journey to discern patterns, relationships, and trends within the data.

- The project's scope is wide-ranging and captivating. The analysis begins by identifying the top 10 most and least popular songs on Spotify, unearthing the spectrum of musical tastes and preferences. Through the utilization of a correlation heatmap, the intricate relationships between various audio features are unveiled, shedding light on the nuances of musical compositions.

- Further exploration is conducted through regression plots, where correlations between specific audio attributes are closely examined. The analysis delves into the connection between loudness and energy, as well as the interplay between popularity and acousticness, unearthing underlying trends that drive listeners' engagement.

The project then pivots to investigate the temporal dimension, visualizing the distribution of songs on Spotify since 1992. The change in song duration over the years is meticulously charted, revealing shifts and trends in musical composition styles. The analysis extends to dissecting song duration across different genres, providing a captivating narrative of how genres evolve and adapt over time.

- Perhaps most intriguingly, the project unveils the top five genres by popularity, painting a vivid picture of musical trends that captivate audiences globally. This segment of the analysis sheds light on the dynamic landscape of music consumption and how certain genres maintain an enduring allure.






![Spotify music collage](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/8a91b159-c7df-4553-ac05-45428cc353f4)









- In conclusion, this exploratory data analysis project offers a multifaceted and captivating journey into the world of music through the lens of data. Leveraging Python's prowess and an array of sophisticated libraries, the project's in-depth examination of Spotify's dataset empowers us to decipher the intricate tapestry of musical trends, preferences, and influences that have shaped the sonic landscape over the years. Through its multifarious visualizations and comprehensive insights, this project resonates as an ode to the intersection of technology and artistry, offering a harmonious symphony of data-driven exploration.







### Objective
 
1. **Top 10 most popular songs on Spotify**


![top 10](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/cd81f3f5-facb-4d0e-b1da-b60789442352)

Image is for reference only

2. [**Top 10 least popular songs on Spotify**](https://open.spotify.com/embed?uri=spotify:user:jaredlosow:playlist:5RrnynsUSNhTIecRySDYhX&view=list)
 
3. **Correlation Heatmap between Variable**

 ![Correlation Heatmap between Variable](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/667f1f6e-dc5b-4206-ac4e-ec2cdf705e50)


4. **Regression plot - Correlation between Loudness and Energy**

![Regression plot - Correlation between Loudness and Energy](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/f4e596f7-f9fc-4fc4-b237-ae227c5027e6)

 
 
5. **Regression plot - Correlation between Popularity and Acousticness**
![Regression plot - Correlation between Popularity and Acousticness](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/e9d61bb0-b002-4e61-81bf-33096d02fb9c)

 
6. **Distibution plot - Visualize total number of songs on Spotify since 1992**
![Distibution plot - Visualize total number of songs on Spotify since 1992](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/39c4e1df-26fb-48a4-b6c3-339b2f6aa6e0)

 
7. **Change in Duration of songs wrt Years**
 ![Change in Duration of songs wrt Years](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/e92c1eb1-9368-464f-b5d2-9b877d32e369)

8. **Duration of songs in different Genres**
 
 
 ![Duration of songs in different Genres](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/0fae7e69-6577-4696-ab18-96ffbf1a4777)

9. **Top 5 Genres by Popularity**
![Top 5 Genres by Popularity](https://github.com/Gokul-Raja84/Spotify-Data-Analysis/assets/106546785/7ec5edd7-a45e-425a-9795-d5d5352947e1)


#### Technologies used ⚙️

***Python***

***Statistics***

***K-Means***

 ##### Python Libraries : 
* <a href="https://pandas.pydata.org/">Pandas</a><a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/450px-Pandas_logo.svg.png" alt="pandas" width="25" height="20"/> </a> |  <a href="https://numpy.org/">NumPy</a><a href="https://numpy.org/" target="_blank" rel="noreferrer"> <img src="https://numpy.org/images/logo.svg" alt="numpy" width="25" height="20"/> </a>  |  <a href="https://matplotlib.org/">Matplotlib</a><a href="https://matplotlib.org/" target="_blank" rel="noreferrer"> <img src="https://matplotlib.org/3.1.1/_static/logo2_compressed.svg" alt="matplotlib" width="25" height="20"/> </a>  |  <a href="https://seaborn.pydata.org">Seaborn</a><a href="https://seaborn.pydata.org" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="Seaborn" width="25" height="20"/> </a>



Kaggle Spotify Datasets:
<code>[Spotify Tracks and Artists](https://www.kaggle.com/datasets/vatsalmavani/spotify-dataset)</code>  
<code>[Spotify Tracks and Artists](https://www.kaggle.com/datasets/gokulraja84/spotify-artists-and-tracks-datasets)</code>   


#### Acknowledgments :

<> The project structure and code implementation were guided by various online resources and tutorials.

<> Feel free to explore the project, modify it according to your needs, and experiment with different approaches to improve the data analysis and data visualization.
