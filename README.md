**Dataset**
- We use `movie.csv`, containing columns like `title`, `overview`, `genres`, etc.

**Setup**
- Python >= 3.7
- `pip install -r requirements.txt` (make sure `nltk`, `pandas`, `numpy`, `scikit-learn` are included)
- (Optional) For full text preprocessing, install `nltk` data:
  ```
  import nltk
  nltk.download('punkt')
  nltk.download('wordnet')
  nltk.download('stopwords')
  ```

**Running**
1. Open this notebook in Jupyter.
2. Run all cells.
3. Call `get_recommendations("I love thrilling action movies set in space, with a comedic twist")`.

**Results**
- The system prints the top recommended items and their similarity scores.
