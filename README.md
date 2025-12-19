# 📚 Book Recommendation Engine using KNN

This project implements a **Book Recommendation System** using the **K-Nearest Neighbors (KNN)** algorithm. It is built in **Python** and designed to run seamlessly in **Google Colaboratory**.

The goal is to recommend books that are similar to a given book based on user rating patterns.

---

## 🧠 Project Overview

The recommendation engine uses **collaborative filtering** to find books similar to a selected title. Similarity is calculated using distance metrics provided by `NearestNeighbors` from `sklearn.neighbors`.

The project uses the **Book-Crossings dataset**, which contains:

* 📖 **270,000 books**
* 👥 **90,000 users**
* ⭐ **1.1 million ratings** (scale of 1–10)

To ensure statistical significance and better recommendations:

* Users with fewer than **200 ratings** are removed
* Books with fewer than **100 ratings** are removed

---

## 🛠️ Technologies Used

* Python
* Google Colaboratory
* NumPy
* Pandas
* SciKit-Learn (`NearestNeighbors`)
* Sparse matrices

---

## ⚙️ How It Works

1. The dataset is preloaded into the notebook.
2. Data is cleaned and filtered based on rating frequency.
3. A user-book matrix is created and converted into a sparse matrix.
4. The **KNN model** finds the nearest neighbors (most similar books).
5. Recommendations are returned based on distance scores.

---

## 📌 Function: `get_recommends(book_title)`

This function takes a **book title** as input and returns:

* The queried book title
* A list of **five similar books**, each paired with its distance score

### Example:

```python
get_recommends("The Queen of the Damned (Vampire Chronicles (Paperback))")
```

### Output Format:

```python
[
  "The Queen of the Damned (Vampire Chronicles (Paperback))",
  [
    ["Catch 22", 0.79],
    ["The Witching Hour (Lives of the Mayfair Witches)", 0.74],
    ["Interview with the Vampire", 0.73],
    ["The Tale of the Body Thief", 0.53],
    ["The Vampire Lestat", 0.51]
  ]
]
```

Lower distance values indicate **higher similarity**.

---

## 🧪 Testing

The final cell in the notebook is reserved for testing.
All implementation code should be written **between the import cells and the test cell**.

---

## 🚀 Getting Started

1. Open the notebook in **Google Colab**
2. Create a copy in your own account
3. Run the cells in order
4. Ensure all tests pass
5. Enable link sharing if submitting the Colab notebook

---

## 📖 Notes

* Graphing the dataset is optional but helpful for understanding sparsity
* Most books are rated infrequently, making filtering essential
* This project is part of a **machine learning certification challenge**

---

Now go commit this like you mean it.
Your repository deserves to look competent. 🦇
