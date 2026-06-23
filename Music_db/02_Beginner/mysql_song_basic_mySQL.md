Table songs {
  song_id int [pk, increment]
  title varchar(255) [not null]
  artist varchar(255) [not null]
  album varchar(255)
  genre varchar(100)
  description text
  duration_seconds int
  release_year int
  play_count int [default: 0]
  created_at timestamp
}