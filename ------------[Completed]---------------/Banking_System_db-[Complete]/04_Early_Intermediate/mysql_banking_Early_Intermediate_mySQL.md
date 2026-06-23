Table transactions {
  transaction_id int [pk, increment]
  account_id int
  amount decimal
  type varchar(50)
}
