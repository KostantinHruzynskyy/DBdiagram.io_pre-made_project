Table achievements {
  achievement_id int [pk, increment]
  game_id int
  name varchar(255)
}

Ref: achievements.game_id > games.game_id
