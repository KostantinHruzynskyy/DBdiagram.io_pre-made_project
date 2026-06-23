Table bookings {
  booking_id int [pk, increment]
  passenger_id int
  flight_id int
}

Ref: bookings.passenger_id > passengers.passenger_id
Ref: bookings.flight_id > flights.flight_id
