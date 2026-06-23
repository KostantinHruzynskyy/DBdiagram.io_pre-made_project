Table users {
  user_id int [pk, increment]
  username varchar(100)
  email varchar(255)
  created_at timestamp
}

Table posts {
  post_id int [pk, increment]
  user_id int
  content text
  created_at timestamp
}

Table comments {
  comment_id int [pk, increment]
  post_id int
  user_id int
  content text
}

Table likes {
  like_id int [pk, increment]
  post_id int
  user_id int
}

Table follows {
  follower_id int
  following_id int
}

Table messages {
  message_id int [pk, increment]
  sender_id int
  receiver_id int
  content text
}

Ref: posts.user_id > users.user_id
Ref: comments.post_id > posts.post_id
Ref: comments.user_id > users.user_id
Ref: likes.post_id > posts.post_id
Ref: likes.user_id > users.user_id
Ref: follows.follower_id > users.user_id
Ref: follows.following_id > users.user_id
Ref: messages.sender_id > users.user_id
Ref: messages.receiver_id > users.user_id
