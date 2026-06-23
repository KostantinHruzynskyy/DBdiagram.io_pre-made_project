Table follows {
  follower_id int
  following_id int
}

Ref: follows.follower_id > users.user_id
Ref: follows.following_id > users.user_id
