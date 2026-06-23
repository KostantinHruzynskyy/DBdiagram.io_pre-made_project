Table songs {
  song_id int [pk, increment]
  title varchar(255)
  genre_id int
}

Table genres {
  genre_id int [pk, increment]
  name varchar(100)
}

Ref: songs.genre_id > genres.genre_id