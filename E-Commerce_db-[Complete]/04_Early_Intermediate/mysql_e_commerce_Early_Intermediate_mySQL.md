Table customers {
  customer_id int [pk, increment]
  name varchar(255)
}

Table orders {
  order_id int [pk, increment]
  customer_id int
}

Ref: orders.customer_id > customers.customer_id
