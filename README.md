# Spotify Popularity Prediction

## Overview
This project explores the relationship between a song's audio characteristics and its popularity on Spotify. Using a dataset of over 89,000 tracks, we built machine learning models to determine if "hits" can be predicted purely through sound data.

## The Problem
Can audio features alone (like danceability, energy, and tempo) explain and predict a song’s popularity score?

## Dataset
The [Spotify Tracks Dataset](https://huggingface.co/datasets/maharshipandya/spotify-tracks-dataset) was utilized for this analysis.
- **Samples:** ~114,000 (Original) | ~89,741 (After removing duplicates)
- **Features:** 11 numerical audio traits (Loudness, Valence, Acousticness, etc.)
- **Target:** `popularity` (0-100)

## Models & Evaluation
We compared a simple linear baseline against a complex non-linear ensemble:
- **Linear Regression** (Baseline)
- **Random Forest Regressor** (Final Model)

### Performance Metrics:
| Model | RMSE | R² Score |
| :--- | :--- | :--- |
| Linear Regression | 20.13 | 0.0300 |
| **Random Forest** | **17.76** | **0.2453** |

## Key Findings
- **Non-Linearity:** Random Forest significantly outperformed Linear Regression, proving that the factors driving music popularity are not simple linear relationships.
- **The "External" Factor:** Our models explain ~25% of popularity variance. This suggests that while sound matters, **75% of success** is likely driven by external factors like artist fame, marketing budgets, and viral social media trends.

## Project Structure
.
├── spp.ipynb              # Main Jupyter Notebook
├── spotify_dataset.csv    # Dataset file
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation

## How to Run
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
