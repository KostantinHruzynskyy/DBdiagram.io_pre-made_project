Table artists {
  artist_id int [pk, increment]
  name varchar(255)
}

Table albums {
  album_id int [pk, increment]
  name varchar(255)
  artist_id int
}

Table songs {
  song_id int [pk, increment]
  title varchar(255)
  artist_id int
  album_id int
}

Ref: albums.artist_id > artists.artist_id
Ref: songs.artist_id > artists.artist_id
Ref: songs.album_id > albums.album_id