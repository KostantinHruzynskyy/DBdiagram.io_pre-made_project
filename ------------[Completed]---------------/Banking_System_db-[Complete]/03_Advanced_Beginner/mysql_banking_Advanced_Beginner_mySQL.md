Table customers {
  customer_id int [pk, increment]
  name varchar(255)
}

Table accounts {
  account_id int [pk, increment]
  customer_id int
  balance decimal
}

Ref: accounts.customer_id > customers.customer_id
