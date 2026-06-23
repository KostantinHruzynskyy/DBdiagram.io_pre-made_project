Table users {
  user_id int [pk, increment]
  name varchar(255)
  role varchar(50)
}

Table rides {
  ride_id int [pk, increment]
  rider_id int
  driver_id int
}

Ref: rides.rider_id > users.user_id
Ref: rides.driver_id > users.user_id
