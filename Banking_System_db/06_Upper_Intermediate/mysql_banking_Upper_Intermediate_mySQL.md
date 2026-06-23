Table cards {
  card_id int [pk, increment]
  account_id int
  type varchar(50)
  limit_amount decimal
}
