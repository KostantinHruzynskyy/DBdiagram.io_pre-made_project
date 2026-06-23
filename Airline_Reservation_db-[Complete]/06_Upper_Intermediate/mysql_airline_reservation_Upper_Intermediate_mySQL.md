Table flights {
  flight_id int [pk, increment]
  departure_airport_id int
  arrival_airport_id int
}

Ref: flights.departure_airport_id > airports.airport_id
Ref: flights.arrival_airport_id > airports.airport_id
