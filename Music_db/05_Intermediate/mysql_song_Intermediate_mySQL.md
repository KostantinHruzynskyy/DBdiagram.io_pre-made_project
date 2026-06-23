Table songs {
  song_id int [pk, increment]
  title varchar(255)
}

Table playlists {
  playlist_id int [pk, increment]
  name varchar(255)
}

Table playlist_songs {
  id int [pk, increment]
  playlist_id int
  song_id int
}

Ref: playlist_songs.playlist_id > playlists.playlist_id
Ref: playlist_songs.song_id > songs.song_id