# Movie Recommendation System — Internship Project

## Project Overview
This project implements a **content-based movie recommendation system** using movie metadata. The system represents each movie using selected descriptive fields and recommends movies with similar content.

## Methodology
- Load `movies.csv`
- Select `genres`, `keywords`, `tagline`, `cast`, and `director`
- Replace missing selected values with empty strings
- Combine the five fields into `combined_features`
- Convert text into numerical vectors with **TF-IDF**
- Calculate movie-to-movie similarity with **cosine similarity**
- Match a user's movie title using Python `difflib`
- Rank and display the most similar movies

## Dataset
The supplied project documentation reports **4,803 movie records and 24 columns**. The recommendation calculation uses five selected attributes:
- genres
- keywords
- tagline
- cast
- director

### Dataset note
The original `movies.csv` file is not present in the currently available files, so it is **not fabricated or substituted** in this package. Place the same `movies.csv` used with the original project in the project folder before running the notebook.

## Expected Result
The supplied project reports a **4,803 × 4,803 cosine-similarity matrix** and demonstrates the query `iron man`. Exact recommendation rankings should be generated from the actual `movies.csv` when the notebook is executed.

## Technologies
- Python
- Pandas
- NumPy
- scikit-learn
- difflib
- Jupyter Notebook

## Files
- `Movie_Recommendation_System_Internship.ipynb` — cleaned internship-ready notebook
- `Movie_Recommendation_System_Original.ipynb` — supplied source notebook
- `README.md` — project documentation
- `requirements.txt` — Python dependencies
- `Diabetes...` files are not part of this project

## Run
```bash
pip install -r requirements.txt
jupyter notebook Movie_Recommendation_System_Internship.ipynb
```

Then ensure `movies.csv` is in the same folder.

## Project Limitations
- Depends on the quality and completeness of movie metadata.
- Does not model collaborative user behaviour.
- Similarity is based on selected textual metadata.
- A full pairwise similarity matrix can require substantial memory for larger catalogues.
- The supplied project does not document a formal offline recommendation-accuracy evaluation.

## Future Scope
- Web or mobile interface
- Hybrid content + collaborative filtering
- Better NLP or embedding-based representations
- User profiles and feedback
- Scalable nearest-neighbour retrieval
- Formal evaluation using suitable relevance data and metrics such as Precision@K, Recall@K, or NDCG

## Academic Note
This package is based on the supplied Movie Recommendation System notebook and project materials and is intended for academic/internship demonstration. It should be presented as a recommendation prototype, not as a claim of production-level recommendation performance.
