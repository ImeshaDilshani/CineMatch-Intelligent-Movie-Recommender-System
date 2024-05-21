<div align="center">
<img style="width: 100%; height: 400px;" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/5298bac0-b8bf-4c80-af67-725c1272dbb0/debo8je-1dc27c90-c1b7-4d88-ba2e-f5e06dab2cb5.jpg/v1/fill/w_1192,h_670,q_70,strp/2021_movie_posters_by_thekingblader995_debo8je-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTA4MCIsInBhdGgiOiJcL2ZcLzUyOThiYWMwLWI4YmYtNGM4MC1hZjY3LTcyNWMxMjcyZGJiMFwvZGVibzhqZS0xZGMyN2M5MC1jMWI3LTRkODgtYmEyZS1mNWUwNmRhYjJjYjUuanBnIiwid2lkdGgiOiI8PTE5MjAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.Ivry10p0hjCIWNMvcVMQrp-nCwNg2pqHzjqLHSEAASw"/>

<h1> 🎬 Content Base Movie Recommender System</h1>
<p style="font-size:20 px;"> <i> This repository contains the code for a content-based movie recommender system using cosine similarity. The project leverages metadata from movies to suggest similar movies based on their content. This type of recommender system is particularly useful for recommending items with similar attributes and providing personalized suggestions to users.</i></p>
</div>

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![NumPy](https://img.shields.io/badge/NumPy-1.19.5-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.1.5-green.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-yellow.svg)
![NLTK](https://img.shields.io/badge/NLTK-3.5-red.svg)

## Data Collection 📥 

The data used in this project comes from the TMDB Movie Dataset available on Kaggle. This dataset consists of two files `tmdb_5000_credits.csv` and `tmdb_5000_movies.csv`.
- Dataset from Kaggle: [TMDB Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata/data)
- Merged datasets based on the movie title.
These files contain comprehensive information about over 5,000 movies, including their cast, crew, plot keywords, genres, and more.

## Important Columns Used 📝 

- id
- title
- overview
- genres
- keywords
- cast
- crew

## Data Preprocessing 🧹 
Preprocessing is a crucial step in any machine learning project. In this stage, I
- Removed missing values and duplicates.
- Converted string data to lists.
- Removed spaces in names and concatenated columns to create a `tags` column.
- Converted `tags` to lowercase.
- Applied stemming to reduce words to their root form (e.g., "loved", "loving", and "love" become "love").

## Feature Engineering 🛠️
Extracted important features from the dataset to create a comprehensive ```tags``` column. This column combines various textual data such as cast, crew, genres, and keywords into a single field, which serves as the input for our model.

## Vectorization and Similarity Calculation

- Used `CountVectorizer` from scikit-learn to convert text data into vectors.
- Calculated cosine similarity between movie vectors.

## Recommendation Function 🎥
A function is created to recommend movies based on the cosine similarity scores. Given a movie title, the function returns a list of similar movies, helping users discover new content based on their preferences.

## 💡 Example
```python
recommend('Spider-Man')
Output:
- Spider-Man 3
- Spider-Man 2
- The Amazing Spider-Man 2
- Arachnophobia
- Kick-Ass
```
