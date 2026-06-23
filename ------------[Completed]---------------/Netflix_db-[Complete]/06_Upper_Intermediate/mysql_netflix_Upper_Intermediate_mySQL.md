Table movies {
  movie_id int [pk, increment]
  title varchar(255)
  genre_id int
}

Table genres {
  genre_id int [pk, increment]
  name varchar(100)
}

Table reviews {
  id int [pk, increment]
  movie_id int
  rating int
}

Ref: movies.genre_id > genres.genre_id
Ref: reviews.movie_id > movies.movie_id