Table customers {
  customer_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table categories {
  category_id int [pk, increment]
  name varchar(100)
}

Table products {
  product_id int [pk, increment]
  category_id int
  name varchar(255)
  price decimal
  stock int
}

Table orders {
  order_id int [pk, increment]
  customer_id int
  total decimal
  status varchar(50)
}

Table order_items {
  id int [pk, increment]
  order_id int
  product_id int
  quantity int
}

Table payments {
  payment_id int [pk, increment]
  order_id int
  amount decimal
}

Ref: products.category_id > categories.category_id
Ref: orders.customer_id > customers.customer_id
Ref: order_items.order_id > orders.order_id
Ref: order_items.product_id > products.product_id
Ref: payments.order_id > orders.order_id
