Table libraries {
  library_id int [pk, increment]
  user_id int
  game_id int
}

Ref: libraries.user_id > users.user_id
Ref: libraries.game_id > games.game_id
