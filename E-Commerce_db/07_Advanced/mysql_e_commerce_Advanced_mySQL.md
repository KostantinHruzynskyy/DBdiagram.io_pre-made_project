Table payments {
  payment_id int [pk, increment]
  order_id int
  amount decimal
  method varchar(50)
}
