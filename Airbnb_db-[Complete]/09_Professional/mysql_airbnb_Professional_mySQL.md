Table users {
  user_id int [pk, increment]
  name varchar(255)
}

Table properties {
  property_id int [pk, increment]
  owner_id int
}

Table bookings {
  id int [pk, increment]
  user_id int
  property_id int
  status varchar(50)
}

Table reviews {
  id int [pk, increment]
  booking_id int
  rating int
}

Ref: properties.owner_id > users.user_id
Ref: bookings.user_id > users.user_id
Ref: bookings.property_id > properties.property_id
Ref: reviews.booking_id > bookings.id