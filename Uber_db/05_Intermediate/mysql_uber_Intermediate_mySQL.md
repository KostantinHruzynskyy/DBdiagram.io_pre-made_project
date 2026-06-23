Table riders {
  rider_id int [pk, increment]
  name varchar(255)
}

Table rides {
  ride_id int [pk, increment]
  rider_id int
  driver_id int
  status varchar(50)
}

Ref: rides.rider_id > riders.rider_id
