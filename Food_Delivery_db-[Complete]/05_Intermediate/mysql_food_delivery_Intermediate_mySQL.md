Table orders {
  order_id int [pk, increment]
  customer_id int
  restaurant_id int
  total decimal
}

Ref: orders.customer_id > customers.customer_id
Ref: orders.restaurant_id > restaurants.restaurant_id
