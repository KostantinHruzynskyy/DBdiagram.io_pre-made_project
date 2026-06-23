Table customers {
  customer_id int [pk, increment]
  name varchar(255)
}

Table accounts {
  account_id int [pk, increment]
  balance decimal
}
