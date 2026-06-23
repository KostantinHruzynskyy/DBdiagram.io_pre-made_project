Table users {
  user_id int [pk, increment]
  email varchar(255)
}

Table subscriptions {
  sub_id int [pk, increment]
  user_id int
  plan varchar(50)
}

Ref: subscriptions.user_id > users.user_id