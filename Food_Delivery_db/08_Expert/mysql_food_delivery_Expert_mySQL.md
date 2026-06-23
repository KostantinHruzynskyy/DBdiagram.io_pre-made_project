Table reviews {
  review_id int [pk, increment]
  customer_id int
  restaurant_id int
  rating int
}

Ref: reviews.customer_id > customers.customer_id
Ref: reviews.restaurant_id > restaurants.restaurant_id
