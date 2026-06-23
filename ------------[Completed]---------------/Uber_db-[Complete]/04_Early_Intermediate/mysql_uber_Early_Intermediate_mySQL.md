Table drivers {
  driver_id int [pk, increment]
  name varchar(255)
  rating decimal
}

Table rides {
  ride_id int [pk, increment]
  driver_id int
  price decimal
}
