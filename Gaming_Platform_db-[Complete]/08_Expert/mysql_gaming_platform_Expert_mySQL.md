Table friends {
  user_id int
  friend_id int
}

Ref: friends.user_id > users.user_id
Ref: friends.friend_id > users.user_id
