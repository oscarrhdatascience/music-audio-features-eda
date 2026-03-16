# Electronic Music Data Analysis

This project explores a large dataset of electronic music tracks by combining **Spotify audio features** with **Beatport track metadata**.

The objective is to build a structured analytical dataset and analyze musical characteristics such as **energy, danceability, tempo, loudness and valence** across millions of tracks.

The repository progressively develops a small **data science workflow** including:

* Exploratory Data Analysis (EDA)
* Data integration across multiple relational datasets
* Feature engineering
* Construction of an analytical dataset for downstream analysis

The final integrated dataset contains **more than 14.5 million electronic music tracks**.

---

# Dataset

The dataset used in this project comes from Kaggle:

https://www.kaggle.com/datasets/mcfurland/10-m-beatport-tracks-spotify-audio-features

It combines information from two main sources:

## Beatport

* Track metadata
* Genres and subgenres
* Release information
* BPM values

## Spotify

* Audio features extracted using the Spotify API

Examples of musical descriptors available in the dataset:

* danceability
* energy
* tempo
* valence
* loudness
* acousticness
* instrumentalness
* liveness
* speechiness

These variables describe different musical aspects such as rhythm, intensity, and emotional tone.

**Note**

The raw dataset is not included in this repository due to its size.  
It can be downloaded directly from the Kaggle link above.

---

# Project Pipeline

The project follows a simple **data science workflow**:

1. Raw Data (Beatport + Spotify)
2. Exploratory Data Analysis
3. Data Integration
4. Data Cleaning
5. Feature Engineering
6. Analytical Dataset (14.5M tracks)
7. Exploratory and Statistical Analysis

During the integration stage, duplicated identifiers from the Beatport catalog are resolved by prioritizing rows with valid BPM values.  
This ensures that each row in the analytical dataset represents a **single unique track identified by its ISRC code**.

---

# Project Notebooks

## 01 — Audio Features EDA

Initial exploration of Spotify audio features including:

* dataset inspection
* missing value analysis
* statistical summaries
* feature distributions
* correlation analysis
* relationships between musical variables
* BPM distribution

Notebook:

https://github.com/oscarrhdatascience/electronic-music-data-analysis/blob/main/notebooks/01_audio_features_eda.ipynb

---

## 02 — Data Integration and Feature Engineering

This notebook integrates Spotify audio features with Beatport metadata.

Key steps:

* inspection of relational dataset structure
* identification of common identifiers (ISRC)
* merging Spotify and Beatport tables
* cleaning duplicated identifiers
* feature engineering for musical characteristics
* construction of a processed analytical dataset

Derived features include:

* **tempo_category** (tempo ranges)
* **energy_level** (energy intensity groups)
* **duration_min** (track duration in minutes)

The resulting dataset contains **14.5 million tracks** ready for further analysis.

Notebook:

https://github.com/oscarrhdatascience/electronic-music-data-analysis/blob/main/notebooks/02_data_integration_and_feature_engineering.ipynb

---

## 03 — Genre Audio Analysis

This notebook analyzes musical characteristics across electronic music genres using the integrated dataset.

Main analyses include:

* BPM comparison across genres
* Energy and danceability ranking
* Musical key distribution
* Loudness comparison between genres
* Correlation analysis between Spotify audio features

These analyses provide insight into how musical characteristics vary across electronic music styles such as Techno, House, Trance and Drum & Bass.

Notebook:

https://github.com/oscarrhdatascience/electronic-music-data-analysis/blob/main/notebooks/03_genre_audio_analysis.ipynb

---

## 04 — Genre Feature Space and Clustering

This notebook explores the structure of electronic music in a high-dimensional feature space using dimensionality reduction and clustering techniques.

Main steps include:

* feature standardization
* Principal Component Analysis (PCA)
* visualization of tracks in a reduced feature space
* interpretation of musical dimensions captured by PCA
* K-Means clustering of tracks
* analysis of the relationship between clusters and music genres

The results reveal that clusters do not strictly correspond to individual genres but rather to **underlying musical characteristics** such as energy level, instrumental content, and vocal presence.

Notebook:

https://github.com/oscarrhdatascience/electronic-music-data-analysis/blob/main/notebooks/04_genre_feature_space_and_clustering.ipynb

---
# Analytical Dataset

The processed dataset contains the following types of variables:

### Track identifiers

* spotify_track_id
* track_title
* isrc

### Metadata

* genre_name
* subgenre_name
* bpm
* duration_min

### Spotify audio features

* acousticness
* danceability
* energy
* instrumentalness
* key
* liveness
* loudness
* mode
* speechiness
* tempo
* time_signature
* valence

### Engineered features

* tempo_category
* energy_level

This dataset serves as the foundation for subsequent musical analysis and machine learning experiments.

---

# Tools and Technologies

The project is implemented using:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Scikit-learn

---

# Project Structure

```
electronic-music-data-analysis
│
├── data
│   ├── raw
│   └── processed
│
├── notebooks
│   ├── 01_audio_features_eda.ipynb
│   └── 02_data_integration_and_feature_engineering.ipynb
│   └── 03_genre_audio_analysis.ipynb
│   └── 04_genre_feature_space_and_clustering.ipynb
│
├── src
│
├── requirements.txt
└── README.md
```

---

# Future Work

Possible extensions of this project include:

* deeper analysis of cluster musical characteristics
* genre classification models using audio features
* recommendation systems based on musical similarity
* temporal analysis of genre evolution
* exploration of additional unsupervised learning techniques

---

# Author

Óscar Rodríguez Hernández  
Data Science Student — UNIR

This project is part of my personal portfolio while developing practical skills in **data analysis, data engineering and machine learning**.