Table comments {
  comment_id int [pk, increment]
  post_id int
  user_id int
  content text
}

Ref: comments.post_id > posts.post_id
Ref: comments.user_id > users.user_id
