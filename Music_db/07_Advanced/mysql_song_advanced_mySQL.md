Table artists {
  artist_id int [pk, increment]
  artist_name varchar(255) [not null]
  country varchar(100)
  created_at timestamp
}

Table albums {
  album_id int [pk, increment]
  artist_id int [not null]
  album_name varchar(255) [not null]
  release_date date
  created_at timestamp
}

Table genres {
  genre_id int [pk, increment]
  genre_name varchar(100) [not null, unique]
}

Table songs {
  song_id int [pk, increment]
  title varchar(255) [not null]
  artist_id int [not null]
  album_id int
  genre_id int
  duration_seconds int
  track_number int
  release_date date
  file_path varchar(500)
  play_count int [default: 0]
  likes_count int [default: 0]
  created_at timestamp
  updated_at timestamp
}

Table playlists {
  playlist_id int [pk, increment]
  playlist_name varchar(255) [not null]
  description text
  created_at timestamp
}

Table playlist_songs {
  playlist_song_id int [pk, increment]
  playlist_id int [not null]
  song_id int [not null]
  position int
  added_at timestamp
}

Ref: albums.artist_id > artists.artist_id
Ref: songs.artist_id > artists.artist_id
Ref: songs.album_id > albums.album_id
Ref: songs.genre_id > genres.genre_id
Ref: playlist_songs.playlist_id > playlists.playlist_id
Ref: playlist_songs.song_id > songs.song_id