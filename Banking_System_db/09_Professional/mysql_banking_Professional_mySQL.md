Table customers {
  customer_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table accounts {
  account_id int [pk, increment]
  customer_id int
  type varchar(50)
  balance decimal
}

Table transactions {
  transaction_id int [pk, increment]
  account_id int
  amount decimal
  type varchar(50)
  created_at timestamp
}

Table loans {
  loan_id int [pk, increment]
  customer_id int
  amount decimal
  status varchar(50)
}

Table cards {
  card_id int [pk, increment]
  account_id int
  card_type varchar(50)
}

Ref: accounts.customer_id > customers.customer_id
Ref: transactions.account_id > accounts.account_id
Ref: loans.customer_id > customers.customer_id
Ref: cards.account_id > accounts.account_id
