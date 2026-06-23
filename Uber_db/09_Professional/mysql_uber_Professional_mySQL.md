Table users {
  user_id int [pk, increment]
  name varchar(255)
  role varchar(50)
}

Table drivers {
  driver_id int [pk, increment]
  user_id int
}

Table rides {
  ride_id int [pk, increment]
  rider_id int
  driver_id int
  status varchar(50)
  start_time timestamp
}

Table payments {
  payment_id int [pk, increment]
  ride_id int
  amount decimal
}

Table ratings {
  id int [pk, increment]
  ride_id int
  score int
}

Ref: drivers.user_id > users.user_id
Ref: rides.rider_id > users.user_id
Ref: rides.driver_id > drivers.driver_id
Ref: payments.ride_id > rides.ride_id
Ref: ratings.ride_id > rides.ride_id
