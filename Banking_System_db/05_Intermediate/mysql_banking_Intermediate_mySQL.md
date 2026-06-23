Table customers {
  customer_id int [pk, increment]
  name varchar(255)
}

Table accounts {
  account_id int [pk, increment]
  customer_id int
  balance decimal
}

Table transactions {
  transaction_id int [pk, increment]
  account_id int
  amount decimal
}

Ref: accounts.customer_id > customers.customer_id
Ref: transactions.account_id > accounts.account_id
