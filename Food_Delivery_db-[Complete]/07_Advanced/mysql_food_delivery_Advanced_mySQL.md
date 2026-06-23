Table payments {
  payment_id int [pk, increment]
  order_id int
  amount decimal
}

Ref: payments.order_id > orders.order_id
