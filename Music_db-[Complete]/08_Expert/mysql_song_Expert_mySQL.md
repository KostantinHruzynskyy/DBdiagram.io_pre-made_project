Table users {
  user_id int [pk, increment]
  username varchar(255)
}

Table songs {
  song_id int [pk, increment]
  title varchar(255)
  artist_id int
}

Table playlists {
  playlist_id int [pk, increment]
  user_id int
  name varchar(255)
}

Table playlist_songs {
  id int [pk, increment]
  playlist_id int
  song_id int
}

Ref: playlists.user_id > users.user_id
Ref: playlist_songs.playlist_id > playlists.playlist_id
Ref: playlist_songs.song_id > songs.song_id