

 # Movie Predictor
                                                

In this project we use TMDB dataset to recommend top 5 similar movies to user, according to the input movie given by the user.

## How to use:

1. Download the dataset (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv)

2. Run the mvpd.ipnb notebook

3. The pickel files will be generated add them to your project with app.py file provided

4. The ML model will run in your browser.
                                             
                                                  
 ## About:
 
1. It is a content based recommender system which reccomends movies according to the similarity of the content input by the user.
2. For the our model we kept genres, id, keywords, overview, cast, crew.
3. we remove language column as approx 95% of the movies are in english, we will also keep the title not original title as original title can be in different language.
4. Since we use similarities of tags we can also drop popularity column as it is a numeric measure.
5. Release date can be a important facator but, for the sake of simplicity of our model we will not incorporate it as it is also of numeric measure.
6. Then, a new column named "tags" will be created by merging the collumns overview, genres, keywords, cast (only top three actors) and crew (only director names).
7. finally our dataset will haave only three columns    -    movie-id, title and tags.

8. Then data is processed (checking for null values and duplicate data)
9. Then using bag of words we will vectorize the tags but we will ignore stopwords.
10. Finally we will find cosine similarity between all the movies and fetch closest 5 movies for the given input movie.

11. Streamlit is used for making the website.
