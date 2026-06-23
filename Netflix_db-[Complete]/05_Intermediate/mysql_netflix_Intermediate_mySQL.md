Table users {
  user_id int [pk, increment]
  name varchar(255)
}

Table watchlist {
  id int [pk, increment]
  user_id int
  movie_id int
}

Ref: watchlist.user_id > users.user_id