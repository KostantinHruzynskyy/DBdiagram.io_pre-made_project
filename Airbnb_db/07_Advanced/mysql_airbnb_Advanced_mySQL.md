Table messages {
  id int [pk, increment]
  sender_id int
  receiver_id int
  text text
}