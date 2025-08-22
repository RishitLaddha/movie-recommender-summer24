
# 🎬 Mini Movie Recommender – Simple, Fun, and Easy

Welcome to my tiny **movie recommendation notebook** built as an early learning project during my first-year summer and later polished for GitHub. It’s a lightweight demo that shows how collaborative filtering works on a small, mock dataset.

---

## 🎯 What’s Inside?

A friendly, notebook-based recommender that:
- Uses a tiny dataset of **30 users** and **10 movies**
- Computes **user–user similarity** with cosine similarity
- Predicts ratings for **unwatched movies**
- Recommends **one best movie** for the selected user

No heavy setup. No big data. Just the core idea, kept super clear.

---

## 🍿 Why I Made It

I wanted a simple way to understand how recommenders think:
- How do “similar users” help make suggestions
- How to predict ratings when data has gaps
- How to keep code small and readable for learning

This is a mini, beginner-friendly notebook you can skim in minutes and still learn the basics.

---

## 📦 Dataset (Mock)

- Users: 30  
- Movies: 10 (Movie1 … Movie10)  
- Ratings: 1 to 5  
- `NaN` means the user hasn’t rated that movie  
- A quick check also lists users who rated all movies

All data is generated inside the notebook. No downloads needed.

---

## 🧠 How It Works

## workflow
<img src="reccomendation.png" alt="Sample Output" width="903" />


**Step 1: Build the ratings table**  
A pandas DataFrame with users as rows and movies as columns.

**Step 2: Pick a user**  
Enter a `UserID` between 1 and 30.

**Step 3: Find similar users**  
Fill missing values with 0 (only for similarity math) and compute **cosine similarity**.

**Step 4: Predict ratings**  
For each unwatched movie:
- Look at ratings from similar users
- Do a **weighted average** using similarity scores
- If nobody rated it, fall back to the movie’s average rating

**Step 5: Recommend**  
Choose the unwatched movie with the highest predicted rating and show it.

---

## 🛠️ Quick Setup

**Requirements**
- Python 3.10 or newer
- Jupyter Notebook
- `pandas`, `numpy`, `scikit-learn`

**Run it**
1. Open the `.ipynb` in Jupyter  
2. Run all cells  
3. When asked, enter a `UserID` from 1 to 30  
4. You’ll get a friendly line like:
```

Recommended Movie for User 1 :--> Movie2 with predicted rating 3.23

```

Tip: Edit the tiny dataset in the notebook if you want to play with different patterns.

---

## ✅ Example

**Input**
```

Enter your User ID (1-30): 1

```

**Output**
```

Recommended Movie for User 1 :--> Movie2 with predicted rating 3.23

```

---

## 📉 Limitations

- Very small, synthetic data set meant for learning  
- No rating normalization or bias handling  
- Treats missing values as 0 for similarity math (simple but not perfect)  
- Returns **one** best recommendation, not a full ranked list

This is intentional to keep things clean and easy to follow.

---

## 🚀 Future Ideas

- Normalize ratings per user before similarity  
- Try **item–item** collaborative filtering and compare  
- Show a **Top-N** list with ties handled nicely  
- Use a real dataset like **MovieLens**  
- Add a tiny **Flask/FastAPI** UI for web-based input

---

## 🔧 Tech Notes

- Python, Jupyter Notebook  
- pandas, numpy, scikit-learn (cosine similarity)  
- Everything lives in one notebook for clarity

---

## 🤝 Contributing

Feel free to explore, fork, and tweak. If you make it smarter or cleaner, that’s a win.

---

## 📝 License

Open source for learning and reuse. Have fun experimenting!
