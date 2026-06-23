Table reviews {
  review_id int [pk, increment]
  user_id int
  game_id int
  rating int
}

Ref: reviews.user_id > users.user_id
Ref: reviews.game_id > games.game_id
