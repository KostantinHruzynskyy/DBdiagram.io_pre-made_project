Table messages {
  message_id int [pk, increment]
  sender_id int
  receiver_id int
  content text
}

Ref: messages.sender_id > users.user_id
Ref: messages.receiver_id > users.user_id
