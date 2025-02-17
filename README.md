# Simple Content-Based Recommendation System

## Overview
This repository contains a simple movie recommendation system that uses TF-IDF vectorization and cosine similarity to suggest movies based on a user’s text query. The system is implemented in a Jupyter Notebook (`recommend.ipynb`) and uses a small dataset of movies (`movies.csv`).

---

## Table of Contents
1. [Dataset](#dataset)
2. [Project Structure](#project-structure)
3. [Installation & Setup](#installation--setup)
4. [How to Run](#how-to-run)
5. [Example Usage](#example-usage)
6. [Demo Video](#demo-video)
7. [Salary Expectation](#salary-expectation)
8. [License](#license)

---

## Dataset
- **File:** `movies.csv`
- **Description:** Contains about 500 rows of movie metadata, including title, overview, original language, vote counts, and average votes.
- **Usage:** The `overview` column is used to build TF-IDF vectors for content-based recommendations.

---

## Project Structure

```
.
├── movies.csv
├── recommend.ipynb
├── requirements.txt
├── demo.md
└── README.md  <-- You are here
```

- **movies.csv**: The movie dataset.  
- **recommend.ipynb**: Main Jupyter Notebook with data loading, preprocessing, TF-IDF vectorization, and the recommendation function.  
- **requirements.txt**: Python dependencies needed to run the notebook.  
- **demo.md**: Contains a link to your screen-recorded demo video (if required).  
- **README.md**: This file (setup instructions and general info).

---

## Installation & Setup

1. **Clone or Download** this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```

2. **Create a Virtual Environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On macOS/Linux
   # or
   venv\Scripts\activate.bat  # On Windows
   ```

3. **Install Dependencies:**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. ** NLTK Downloads:**  
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('wordnet')
   nltk.download('omw-1.4')
   ```

---

## How to Run

### Jupyter Notebook

1. **Launch Jupyter:**
   ```bash
   jupyter notebook
   ```
2. **In your browser, open `recommend.ipynb`.**
3. **Run all cells in order:**
   - Data Loading: Verifies the shape and a preview of the dataset.
   - Preprocessing: Applies text cleaning (lowercasing, punctuation removal, lemmatization).
   - TF-IDF Vectorization: Builds the vector representation of each movie overview.
   - Recommendation Function: Uses cosine similarity to find the most relevant movies for a user query.
   - Test with a custom query at the bottom of the notebook.

---

## Example Usage

Inside `recommend.ipynb` (final cell or a dedicated cell at the end), you might see something like:

```python
user_query = "I love thrilling action movies set in space, with a comedic twist."
recommend_movies(user_query, df, tfidf_matrix, vectorizer, top_n=5)
```

**Output:** A table of the top 5 movie titles with their similarity scores and overviews.

Try changing the query to see different results, e.g.:

```python
"I want a romantic comedy with a quirky lead protagonist."
```

---

## Demo Video

A short screen-capture demo showcasing:
- How you install dependencies
- How you run `recommend.ipynb`
- A sample query and its recommendation output

**Link:** Paste your video link here or in `demo.md`

---

## Salary Expectation

**Monthly Salary Expectation:** $XX,XXX per month.

---

## License

Distributed under the MIT License (or whichever license you prefer).

---

### Notes

- **Customize**: If you have a Python script (e.g., `recommend.py`) instead of a Notebook, adjust the instructions in your README accordingly (e.g., how to run from the command line: `python recommend.py "some user description"`).  
- **License**: If needed, add a separate `LICENSE` file or choose a different open-source license.  
- **Versioning**: If you want stricter reproducibility, pin exact versions in `requirements.txt`.
