# Movie Recommendation System (MovieLens 100K Dataset)

## Project Overview
This project builds a **Movie Recommendation System** using the **MovieLens 100K dataset**.  
The goal is to recommend movies to users based on their preferences and the similarity between users or movies.  
It explores **collaborative filtering** techniques — both **user-based** and **item-based** approaches.

---

## Objective
Develop a system that:
- Recommends movies based on user–movie rating patterns.
- Computes similarity between users or movies.
- Suggests top-rated unseen movies for a given user.
- Evaluates system performance using basic metrics (e.g., Precision@K).

---

## Tools & Libraries
- **Python**
- **Pandas**, **NumPy**
- **Scikit-learn**
- **Google Colab** (for development and testing)

---

## Dataset
- **MovieLens 100K Dataset**
  - 100,000 ratings (1–5 scale)
  - 943 users and 1,682 movies
  - Files used:
    - `u.data` → user ID, movie ID, rating, timestamp  
    - `u.item` → movie ID, title, and metadata  

---

## Project Steps

### 1. Data Loading & Preprocessing
- Load `u.data` and `u.item` files.
- Merge both to include movie names with ratings.
- Handle encoding using `encoding='latin-1'`.
- Explore the dataset (users, movies, rating distribution).

### 2. Building the User–Item Matrix
- Create a matrix where:
  - Rows = users  
  - Columns = movies  
  - Values = ratings  
- Missing ratings remain `NaN` (unrated movies).

### 3. User-Based Collaborative Filtering
- Compute **cosine similarity** between users.
- Identify users with similar preferences.
- Recommend top-rated movies that the target user has not seen yet.

### 4. Item-Based Collaborative Filtering *(Final Step)*
- Compute **cosine similarity** between movies based on user ratings.
- For a given movie, find the most similar ones (e.g., same audience interest or rating pattern).
- Example:
Target Movie: Quiz Show (1994)
Top Similar Movies:

E.T. the Extra-Terrestrial (1982)

Forrest Gump (1994)

Shawshank Redemption, The (1994)
...

### 5. Evaluation
- Used **Precision@K** metric to measure how many recommended movies were actually liked by users.
- Note: Precision@K may be low due to limited ground-truth ratings for unseen movies in the static dataset.

---

## Insights
- **User-Based CF** performs well when user preferences overlap significantly.
- **Item-Based CF** is more stable — movie similarity patterns remain consistent over time.
- Recommendations align with genre, theme, or audience taste.
- Demonstrates how similarity-based approaches can power real-world recommendation systems.

---

## 🚀 Future Improvements
- Implement **Matrix Factorization (SVD)** for latent factor discovery.
- Add **content-based filtering** using movie genres or descriptions.
- Combine methods into a **hybrid recommendation model**.
- Deploy the system as a simple web app (e.g., Flask + Streamlit).

---

## Author
**Kenzy Mohammed**  
*Data Science Enthusiast*  
[linkedin.com/in/kenzy-mohamed-2938852b6](#) | [https://github.com/KenzyMohammed](#)

---

## License
This project is open-source and available under the [MIT License](LICENSE).
