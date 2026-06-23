Table users {
  user_id int [pk, increment]
  username varchar(100)
  email varchar(255)
}

Table games {
  game_id int [pk, increment]
  title varchar(255)
  price decimal
}

Table libraries {
  library_id int [pk, increment]
  user_id int
  game_id int
}

Table achievements {
  achievement_id int [pk, increment]
  game_id int
  name varchar(255)
}

Table reviews {
  review_id int [pk, increment]
  user_id int
  game_id int
  rating int
}

Table purchases {
  purchase_id int [pk, increment]
  user_id int
  total decimal
}

Ref: libraries.user_id > users.user_id
Ref: libraries.game_id > games.game_id
Ref: achievements.game_id > games.game_id
Ref: reviews.user_id > users.user_id
Ref: reviews.game_id > games.game_id
Ref: purchases.user_id > users.user_id
