Table riders {
  rider_id int [pk, increment]
  name varchar(255)
}

Table deliveries {
  delivery_id int [pk, increment]
  order_id int
  rider_id int
}

Ref: deliveries.order_id > orders.order_id
Ref: deliveries.rider_id > riders.rider_id
