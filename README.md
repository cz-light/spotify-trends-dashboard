# Spotify Artist Recommender & Trend Explorer

> Content-based artist recommendation engine combined with
> historical Spotify chart trend analysis — built with the
> Spotify Web API and 4 years of global chart data.

**Live app:** _coming soon_
**Portfolio:** https://cz-light.github.io

---

## Overview

This project has two layers:

1. **Recommender engine** — given a seed artist, finds the 10 most similar artists in the dataset using cosine similarity across 13 audio features (danceability, energy, valence, tempo, etc.) and genre tags. Built with the live Spotify Web API and scikit-learn.

2. **Historical trend analysis** — analyzes 4 years of global Spotify chart data (2017–2021) to identify genre shifts, audio feature trends in popular music, and artist longevity patterns.

---

## Tech stack

- **Language:** Python
- **API:** spotipy (Spotify Web API)
- **Analysis:** pandas · NumPy · scikit-learn
- **Visualization:** Plotly Express · seaborn
- **Dashboard:** Streamlit (3 pages)
- **Deployed:** Streamlit Cloud

---

## Questions this project answers

1. Given an artist I like, who else would I probably enjoy?
2. Which audio features correlate most with chart success?
3. How has the sound of popular music shifted from 2017–2021?
4. Which genres dominated charts and how did that change over time?
5. Who are the most consistent charting artists vs one-hit wonders?

---

## Dashboard pages

- **Artist Recommender** — search any artist, get 10 recommended similar artists with similarity scores and audio feature breakdowns
- **Historical Trends** — genre popularity over time, audio feature shifts by year, regional chart dominance
- **Artist Explorer** — individual artist audio feature radar chart, chart history, and position on danceability vs energy scatter plot

---

## ML pipeline

1. Extract 500+ artists from Kaggle chart data
2. Pull top tracks and audio features per artist via Spotify API
3. Average audio features across top tracks → one feature vector per artist
4. Normalize numeric features with MinMaxScaler, one-hot encode top 50 genres
5. Compute full pairwise cosine similarity matrix with scikit-learn
6. Given a seed artist, return top N most similar by similarity score

---

## Features

- [ ] Artist dataset of 500+ artists with audio feature vectors
- [ ] Normalized feature matrix + cosine similarity model
- [ ] Top 10 artist recommendations per seed input
- [ ] Historical genre trend line charts (2017–2021)
- [ ] Artist longevity analysis (consistent charters vs one-hit wonders)
- [ ] Audio feature trend analysis by year
- [ ] 3-page interactive Streamlit dashboard deployed to Streamlit Cloud
- [ ] Radar chart comparing seed artist vs recommended artists (stretch)
- [ ] Multi-artist blending — average two seed artists (stretch)

---

## Screenshots

_Coming soon_

---

## Local setup

```bash
git clone https://github.com/cz-light/spotify-trends-dashboard
cd spotify-trends-dashboard
python -m venv venv
source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows
pip install -r requirements.txt
```

Add your Spotify API credentials to a `.env` file in the root:

```
SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here
```

Get credentials at: https://developer.spotify.com/dashboard

### Run the dashboard

```bash
streamlit run dashboard/app.py
```

### Run notebooks

```bash
jupyter notebook
```

---

## Data sources

- [Spotify Charts dataset — Kaggle](https://www.kaggle.com/datasets/dhruvildave/spotify-charts) — historical chart data 2017–2021
- [Spotify Web API](https://developer.spotify.com/) — live artist profiles, audio features, genre tags

---

## Project structure

```
spotify-trends-dashboard/
├── data/
│   ├── raw/                 # original datasets (gitignored)
│   └── processed/           # cleaned CSVs and artist feature matrix
├── notebooks/               # Jupyter EDA and model development notebooks
├── src/                     # reusable Python modules
│   ├── data_collection.py   # spotipy API calls
│   ├── features.py          # feature engineering pipeline
│   └── recommender.py       # cosine similarity model
├── dashboard/               # Streamlit app
│   └── app.py
└── docs/
    └── screenshots/
```

---

## What I learned

_To be written on project completion._