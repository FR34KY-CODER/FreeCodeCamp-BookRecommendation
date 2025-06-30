# 📚 Book Recommendation Engine using KNN - FreeCodeCamp

This project builds a book recommendation system using **K-Nearest Neighbors (KNN)** on the Book-Crossing dataset. It recommends similar books based on collaborative filtering.

---

## 🚀 Objective

Create a KNN-based recommender that returns **5 similar books** for any given book title based on user ratings.

---

## 🔧 What We Did

- Preprocessed and filtered the dataset:
  - Users with ≥ 200 ratings
  - Books with ≥ 100 ratings
- Merged book ratings with titles.
- Built a pivot table of book titles (rows) vs users (columns).
- Converted it to a sparse matrix.
- Trained a **cosine similarity-based** KNN model.
- Implemented a `get_recommends(book)` function which returns recommendations in the following format:

```
[
  "Book Title",
  [
    ["Recommended Book 1", distance],
    ["Recommended Book 2", distance],
    ...
  ]
]
```
---

## 🧪 Example Output

```
get_recommends("Where the Heart Is (Oprah's Book Club (Paperback))")

Returns:
```
```
[
  "Where the Heart Is (Oprah's Book Club (Paperback))",
  [
    ["I'll Be Seeing You", 0.801],
    ["The Weight of Water", 0.770],
    ["The Surgeon", 0.769],
    ["I Know This Much Is True", 0.767]
  ]
]
```
---

## ✅ Tech Stack

- Python
- pandas
- scikit-learn
- scipy
- seaborn, matplotlib (for analysis)

---

## 📁 Dataset Used

- `BX-Books.csv`
- `BX-Book-Ratings.csv`  
  *(Already included in the challenge notebook)*

---

## 📌 Note

This project was built for the **freeCodeCamp Machine Learning Certification**.  
The test case only passes when specific book titles and their correct distances are returned.
