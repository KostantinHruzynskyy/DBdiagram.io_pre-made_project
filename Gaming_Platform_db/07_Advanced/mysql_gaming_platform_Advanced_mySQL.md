Table purchases {
  purchase_id int [pk, increment]
  user_id int
  total decimal
}

Ref: purchases.user_id > users.user_id
