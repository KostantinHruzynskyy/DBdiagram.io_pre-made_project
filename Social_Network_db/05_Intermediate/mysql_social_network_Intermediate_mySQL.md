Table likes {
  like_id int [pk, increment]
  user_id int
  post_id int
}

Ref: likes.user_id > users.user_id
Ref: likes.post_id > posts.post_id
