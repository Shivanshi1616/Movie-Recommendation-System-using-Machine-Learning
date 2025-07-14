# Movie-Recommendation-System

# 🎬 Movie Recommendation System 🎥🧠

## 📌 Project Overview  
This project is designed to recommend movies similar to a selected movie using **Content-Based Filtering**.  
It suggests the **Top 5 most similar movies** based on the combination of a movie’s **overview**, **genre**, and **director**, using **TF-IDF Vectorization** and **Cosine Similarity**.

---

## 🎯 Objective  
To build a basic recommender system that suggests movies based on user input using **similarity scores** calculated from textual movie data.

---

## 📑 Dataset Used

- **Source**: IMDb Top 1000 Movies (CSV)
- **Columns in the Dataset:**
  - `Poster_Link`
  - `Series_Title`
  - `Released_Year`
  - `Certificate`
  - `Runtime`
  - `Genre`
  - `IMDB_Rating`
  - `Overview`
  - `Meta_score`
  - `Director`
  - `Star1`, `Star2`, `Star3`, `Star4`
  - `No_of_Votes`
  - `Gross`

---

## ⚙️ Tools & Technologies Used

**Programming Language:**
- Python 🐍

**Python Libraries:**
- `pandas` → Data manipulation and preprocessing  
- `scikit-learn` → TF-IDF vectorization and cosine similarity  
- `TfidfVectorizer` → Transform text data into feature vectors  
- `cosine_similarity` → Measure similarity between movie vectors  

---

## 🔁 Project Workflow

1. **Data Loading:**
   - Loaded the dataset using `pandas.read_csv()`.

2. **Missing Value Handling:**
   - Checked for nulls in important columns like `Director`, `Genre`, and `Overview`.
   - Filled missing values with empty strings to avoid errors during vectorization.

3. **Feature Engineering:**
   - Combined `Director`, `Genre`, and `Overview` into a new feature called `combined_features`.

4. **Vectorization:**
   - Used `TfidfVectorizer(stop_words='english')` to convert combined text into numerical vectors.

5. **Similarity Calculation:**
   - Applied `cosine_similarity()` on the TF-IDF matrix to compute similarity scores between movies.

6. **Recommendation Function:**
   - Created a function that takes a movie title as input and returns the top 5 most similar movies based on cosine similarity.

7. **User Input & Output:**
   - Took a movie name from the user and displayed top recommendations in order of similarity.

---

## ✨ Key Highlights

- **Smart Movie Matching:** Recommends highly relevant movies by analyzing text-based features.
- **Efficient Data Processing:** Leveraged TF-IDF and Cosine Similarity for accurate and fast recommendations.
- **Clean Architecture:** Well-structured notebook using Python and scikit-learn for scalable development.

---

## ❓ Key Questions Addressed by the Recommender

1. How similar is one movie to another based on content?
2. Which 5 movies are closest to a selected movie in terms of storyline and genre?
3. Can we make recommendations using just text data without ratings?

---

## 🚀 Future Enhancements

- Integrate **Streamlit** to build an interactive UI.
- Include features like **Actors**, **Runtime**, and **Ratings** for richer recommendations.
- Add support for **search by director or genre**.
- Combine with **Collaborative Filtering** for a hybrid recommendation system.

---

### **This project uses ML, NLP, and data science techniques to deliver intelligent movie suggestions based on content!** 🎞️🧠👩‍💻👨‍💻
