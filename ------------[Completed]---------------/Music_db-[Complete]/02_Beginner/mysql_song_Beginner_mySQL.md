Table albums {
  album_id int [pk, increment]
  name varchar(255)
}

Table songs {
  song_id int [pk, increment]
  title varchar(255)
  album_id int
}

Ref: songs.album_id > albums.album_id