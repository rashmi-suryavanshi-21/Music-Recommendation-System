# 🎵 Music Recommendation System

A content-based Music Recommendation System built using **Python**, **Streamlit**, and **Machine Learning**. The application recommends similar songs based on song lyrics using **TF-IDF Vectorization** and **Cosine Similarity**.

---

## 🚀 Features

- **Web UI:** Streamlit application with song selection and recommendation trigger.
- **Preprocessing:** Loads the CSV dataset, samples 10,000 songs, cleans text (tokenization and stopword removal), performs TF-IDF vectorization, and saves preprocessed artifacts.
- **Recommendation Engine:** Loads preprocessed artifacts, computes cosine-similarity-based top-N recommendations, and displays recommended songs with artist names.
- **Persistence & Logging:** Stores generated artifacts using Joblib (`df_cleaned.pkl`, `tfidf_matrix.pkl`, `cosine_sim.pkl`) and maintains preprocessing and recommendation logs.

---

## 🛠️ Tech Stack

- Python
- Streamlit
- Pandas
- NLTK
- Scikit-learn
- Joblib

---

## 📂 Project Structure

```
Music_Recommendation/
│
├── README.md
├── requirements.txt
├── Music_Recommendation_System_using_Python_code_prep_2.ipynb
├── start_app.txt
│
└── src/
    ├── main.py
    ├── preprocess.py
    ├── recommend.py
    └── spotify_millsongdata.csv
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd Music_Recommendation
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows**

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Navigate to the `src` directory.

```bash
cd src
```

### Generate preprocessing artifacts

```bash
python preprocess.py
```

This generates:

- `df_cleaned.pkl`
- `tfidf_matrix.pkl`
- `cosine_sim.pkl`

### Launch the Streamlit application

```bash
streamlit run main.py
```

The application will open in your browser at:

```
http://localhost:8501
```

---

## 📖 How It Works

1. Load the Spotify songs dataset.
2. Sample 10,000 songs.
3. Clean and preprocess song lyrics.
4. Convert lyrics into TF-IDF vectors.
5. Compute cosine similarity between songs.
6. Recommend the most similar songs based on the selected song.

---