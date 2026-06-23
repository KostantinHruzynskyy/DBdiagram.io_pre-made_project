Table posts {
  post_id int [pk, increment]
  user_id int
  content text
}

Ref: posts.user_id > users.user_id
