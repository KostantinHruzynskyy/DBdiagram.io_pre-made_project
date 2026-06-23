Table movies {
  movie_id int [pk, increment]
  title varchar(255)
  genre_id int
}

Table users {
  user_id int [pk, increment]
  name varchar(255)
}

Table watch_history {
  id int [pk, increment]
  user_id int
  movie_id int
}

Ref: watch_history.user_id > users.user_id
Ref: watch_history.movie_id > movies.movie_id