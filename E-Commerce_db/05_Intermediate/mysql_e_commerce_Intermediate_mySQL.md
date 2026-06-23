Table products {
  product_id int [pk, increment]
  name varchar(255)
  price decimal
}

Table order_items {
  id int [pk, increment]
  order_id int
  product_id int
  quantity int
}

Ref: order_items.product_id > products.product_id
