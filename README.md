# spotify-family-playlist-reconstruction
Machine learning project that reconstructs missing Spotify family Top-of-the-Year playlists (2019–2025) after a simulated data loss and proposes a recommendation system design for multi-user family accounts.
---

```markdown
# Spotify Family Playlist Reconstruction & Recommendation

This repository contains a machine learning project focused on **Spotify family accounts**, developed as part of a data analytics course project. The project addresses a simulated data-loss scenario in which users’ *Top-of-the-Year playlists (2019–2025)* were deleted and must be reconstructed using song-level data.

The project consists of two main tasks:
1. **Playlist reconstruction (implemented)**
2. **Recommendation algorithm design (conceptual)**

---

## Project Context

After a simulated hacker attack on Spotify servers, only one **mixed playlist** per family account remained, containing songs from all users and years.  
Partial information about which user and which year each song belongs to was recovered, but some songs remain unlabeled.

The goal of this project is to:
- Reconstruct missing playlist information using machine learning
- Design a recommendation system suitable for Spotify family accounts

---

## Task 1 – Playlist Reconstruction (Implemented)

### Objective
Reconstruct each user’s **Top-of-the-Year playlists (2019–2025)** by predicting:
- the **user** each song belongs to
- the corresponding **Top-of-the-Year label**

### Approach
- Use labeled songs as training data
- Extract and preprocess song audio features and metadata
- Train and evaluate supervised machine learning models
- Apply the selected model to predict missing labels
- Generate reconstructed playlists as separate CSV files (one per user per year)

### Output
- Reconstructed playlists saved as CSV files  
  Example naming convention:
```

user_<USERID>*top*<YEAR>.csv

```

---

## Task 2 – Recommendation Algorithm Design (Conceptual)

### Objective
Design a song recommendation approach for **Spotify family accounts** that:
- Uses song characteristics and user preferences
- Accounts for shared listening situations and content restrictions
- Recommends the next song or a ranked list of candidate songs

### Key Ideas
- Two-step recommendation architecture:
1. Candidate generation
2. Machine-learning-based ranking
- Logistic Regression used conceptually for ranking
- Feature justification provided for all inputs

> **Note:** Task 2 is conceptual only and does not include implementation code.

---

## Dataset

### Required File
This project **requires the Spotify mixed playlist dataset**:

```

mixed_playlist.csv

```

⚠️ **Important:**  
The dataset is **not included in this repository** and must be **uploaded manually** before running the notebook.

### Dataset Description
- Total songs: 3,600
- Labeled songs: 3,500 (user + year known)
- Unlabeled songs: 100 (user and year missing)
- Features include audio characteristics and popularity-related metadata

---

## Repository Structure

```

.
├── spotify_project.ipynb        # Main Jupyter notebook (Task 1 & Task 2)
├── reconstructed_playlists/     # Output CSV files (generated)
├── README.md                    # Project documentation

````

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/spotify-family-playlist-reconstruction.git
````

2. Upload `mixed_playlist.csv` to the project directory
3. Open the Jupyter notebook:

   ```bash
   jupyter notebook spotify_project.ipynb
   ```
4. Run all cells from top to bottom

---

## Tools & Technologies

* Python
* Jupyter Notebook
* Pandas, NumPy
* Scikit-learn
* Machine Learning (Classification, Evaluation)

---

## Disclaimer

This project is **for academic purposes only** and is not affiliated with or endorsed by Spotify.

---
