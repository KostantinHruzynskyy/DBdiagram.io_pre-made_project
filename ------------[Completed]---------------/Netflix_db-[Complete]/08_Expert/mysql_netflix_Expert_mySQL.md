Table movies {
  movie_id int [pk, increment]
  title varchar(255)
}

Table actors {
  actor_id int [pk, increment]
  name varchar(255)
}

Table movie_actors {
  id int [pk, increment]
  movie_id int
  actor_id int
}

Ref: movie_actors.movie_id > movies.movie_id
Ref: movie_actors.actor_id > actors.actor_id