Table loans {
  loan_id int [pk, increment]
  customer_id int
  amount decimal
  interest_rate decimal
}

Table customers {
  customer_id int [pk, increment]
  name varchar(255)
}

Ref: loans.customer_id > customers.customer_id
