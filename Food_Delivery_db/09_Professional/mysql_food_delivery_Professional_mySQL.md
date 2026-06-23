Table customers {
  customer_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table restaurants {
  restaurant_id int [pk, increment]
  name varchar(255)
  address varchar(255)
}

Table menu_items {
  item_id int [pk, increment]
  restaurant_id int
  name varchar(255)
  price decimal
}

Table orders {
  order_id int [pk, increment]
  customer_id int
  restaurant_id int
  total decimal
  status varchar(50)
}

Table riders {
  rider_id int [pk, increment]
  name varchar(255)
}

Table deliveries {
  delivery_id int [pk, increment]
  order_id int
  rider_id int
}

Ref: menu_items.restaurant_id > restaurants.restaurant_id
Ref: orders.customer_id > customers.customer_id
Ref: orders.restaurant_id > restaurants.restaurant_id
Ref: deliveries.order_id > orders.order_id
Ref: deliveries.rider_id > riders.rider_id
