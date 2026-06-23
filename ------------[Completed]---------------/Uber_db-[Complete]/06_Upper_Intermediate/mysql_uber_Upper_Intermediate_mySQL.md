Table rides {
  ride_id int [pk, increment]
  rider_id int
  driver_id int
  start_location varchar(255)
  end_location varchar(255)
  distance_km decimal
}
