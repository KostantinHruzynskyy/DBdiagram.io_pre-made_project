Table customers {
  customer_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table orders {
  order_id int [pk, increment]
  customer_id int
  total decimal
}

Table order_items {
  id int [pk, increment]
  order_id int
  product_name varchar(255)
  price decimal
}

Ref: orders.customer_id > customers.customer_id
Ref: order_items.order_id > orders.order_id