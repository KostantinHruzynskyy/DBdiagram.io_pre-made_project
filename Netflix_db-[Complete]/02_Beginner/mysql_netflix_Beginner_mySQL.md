Table movies {
  movie_id int [pk, increment]
  title varchar(255)
  year int
}

Table genres {
  genre_id int [pk, increment]
  name varchar(100)
}

Ref: movies.genre_id > genres.genre_id