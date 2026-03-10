# Exploratory Data Analysis of Electronic Music Tracks

This project explores a large dataset of electronic music tracks combining **Beatport metadata** and **Spotify audio features**.

The goal of this analysis is to understand the structure of the dataset and identify patterns in the musical characteristics of electronic music tracks.

This repository contains the first stage of the project: **Exploratory Data Analysis (EDA)**.

---

# Dataset

The dataset used in this project comes from Kaggle:

https://www.kaggle.com/datasets/mcfurland/10-m-beatport-tracks-spotify-audio-features

It contains more than **10 million tracks** and combines information from two main sources:

- Beatport (metadata about tracks, artists, genres and releases)
- Spotify Audio Features (musical characteristics extracted from the Spotify API)

For this initial analysis we focus on the **audio_features** table, which contains musical descriptors such as:

- danceability
- energy
- tempo
- valence
- loudness
- acousticness
- instrumentalness
- liveness
- speechiness

These variables describe different musical aspects such as rhythm, intensity and emotional tone.

**Note:**  
The raw dataset is not included in this repository due to its size.  
It can be downloaded directly from the Kaggle link above.

---

# Project Objectives

The main goals of this exploratory analysis are:

- Understand the structure of the dataset
- Inspect data types and missing values
- Explore the distribution of key musical features
- Analyze relationships between audio characteristics
- Identify structural patterns in electronic music

---

# Exploratory Data Analysis

The exploratory analysis is implemented in the following notebook:
notebooks/01_audio_features_eda.ipynb


The analysis includes:

- Dataset overview
- Missing value inspection
- Statistical summary of audio features
- Distribution analysis of musical variables
- Correlation analysis between audio features
- Relationship analysis between key variables
- Tempo (BPM) distribution analysis

---

# Key Insights

Some interesting patterns observed in the dataset include:

- Most tracks are concentrated between **120 and 130 BPM**, which aligns with common tempo ranges in electronic dance music.
- A strong relationship exists between **energy and loudness**, reflecting typical mastering practices in electronic music production.
- Tracks tend to show **high danceability values**, consistent with music designed for club environments.
- The relationship between **danceability and valence** suggests that more danceable tracks tend to have slightly more positive emotional characteristics.

These results highlight structural patterns in contemporary electronic music production.

---

# Tools and Technologies

The analysis was performed using:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# Project Structure
music-audio-features-eda
│
├── data
│   ├── raw
│   └── processed
│
├── notebooks
│   └── 01_audio_features_eda.ipynb
│
├── src
│
├── requirements.txt
└── README.md

---

# Future Work

The next stages of this project will include:

- Combining audio features with track metadata
- Genre and subgenre analysis
- Track clustering based on audio characteristics
- Identifying musical patterns using unsupervised learning techniques

---

# Author

Oscar Rodríguez Hernández  
Data Science student

This project is part of my personal portfolio while developing practical skills in **data analysis and machine learning**.
