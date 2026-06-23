Table drivers {
  driver_id int [pk, increment]
  name varchar(255)
}

Table vehicles {
  vehicle_id int [pk, increment]
  driver_id int
  model varchar(100)
}

Table rides {
  ride_id int [pk, increment]
  driver_id int
}

Ref: vehicles.driver_id > drivers.driver_id
Ref: rides.driver_id > drivers.driver_id
