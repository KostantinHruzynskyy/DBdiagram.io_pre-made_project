Table carts {
  cart_id int [pk, increment]
  customer_id int
}

Table cart_items {
  id int [pk, increment]
  cart_id int
  product_id int
}

Ref: cart_items.cart_id > carts.cart_id
