# Spotify Trends Dashboard

> End-to-end analysis of Spotify chart data — audio
> feature trends, genre shifts, and popularity drivers.

**Live app:** _coming soon_
**Portfolio:** https://cz-light.github.io

---

## Tech stack
- **Language:** Python
- **Analysis:** pandas · seaborn · scikit-learn
- **Visualization:** Plotly Express
- **Dashboard:** Streamlit
- **API enrichment:** spotipy (Spotify Web API)
- **Deployed:** Streamlit Cloud

---

## Questions this project answers
1. What audio features correlate most with chart success?
2. How has the sound of popular music changed over the years?
3. Which genres dominate, and are any rising or declining?
4. Who are the most consistent charting artists?
5. Can you predict a song's popularity from audio features?

---

## Features
- [ ] EDA notebook with distributions and correlations
- [ ] Interactive Streamlit dashboard
- [ ] Genre trend line chart with year filter
- [ ] Popularity vs audio feature scatter plots
- [ ] Random Forest popularity prediction model

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

### Run the dashboard
```bash
streamlit run dashboard/app.py
```

### Run notebooks
```bash
jupyter notebook
```

---

## Data source
[Spotify Charts dataset — Kaggle](https://www.kaggle.com/datasets/dhruvildave/spotify-charts)

---

## Project structure
```
spotify-trends-dashboard/
├── data/
│   ├── raw/          # original dataset (gitignored)
│   └── processed/    # cleaned outputs
├── notebooks/        # Jupyter EDA notebooks
├── src/              # reusable Python modules
├── dashboard/        # Streamlit app
│   └── app.py
└── docs/
    └── screenshots/
```

---

## What I learned
_To be written on project completion._