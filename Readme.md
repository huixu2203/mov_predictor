


## Movie Predictor
                                                

In this project, we use the TMDB dataset to recommend the top 5 similar movies to the user, according to the input movie given by the user.


## How to use:

1. Download the dataset (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv).

2. Run the mvpd.ipnb notebook.

3. The pickel files will be generated; add them to your project with the app.py file provided.

4. The ML model will run in your browser.
                                             
 
 
## About:                                                  
1. It is a content-based recommender system that recommends movies according to the similarity of the content input by the user.
2. For our model, we kept genres, id, keywords, overview, cast, and crew.
3. We remove the language column as approximately 95% of the movies are in English. We will also keep the title, not the original title, as the original title can be in a different language.
4. Since we use similarities between tags, we can also drop the popularity column as it is a numeric measure.
5. Release date can be an important factor, but for the sake of simplicity in our model, we will not incorporate it as it is also a numerical measure.
6. Then, a new column named "tags" will be created by merging the columns overview, genres, keywords, cast (only the top three actors), and crew (only director names).
7. Finally, our dataset will have only three columns: movie-id, title, and tags.

8. Then the data is processed (checking for null values and duplicate data).
9. Then, using a bag of words, we will vectorize the tags but ignore stopwords.
10. Finally, we will find the cosine similarity between all the movies and fetch the 5 closest movies for the given input movie.

11. Streamlit is used for making the website.
