Table songs {
  song_id int [pk, increment]
  title varchar(255)
  duration_seconds int
  play_count int
  likes int
  release_year int
}