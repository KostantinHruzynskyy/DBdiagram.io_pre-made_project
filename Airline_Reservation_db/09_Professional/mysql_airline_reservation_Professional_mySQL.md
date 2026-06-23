Table passengers {
  passenger_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table airports {
  airport_id int [pk, increment]
  name varchar(255)
  city varchar(255)
  country varchar(255)
}

Table flights {
  flight_id int [pk, increment]
  flight_number varchar(20)
  departure_airport_id int
  arrival_airport_id int
  departure_time datetime
  arrival_time datetime
}

Table bookings {
  booking_id int [pk, increment]
  passenger_id int
  flight_id int
  booking_date datetime
}

Table tickets {
  ticket_id int [pk, increment]
  booking_id int
  seat_number varchar(10)
}

Ref: bookings.passenger_id > passengers.passenger_id
Ref: bookings.flight_id > flights.flight_id
Ref: flights.departure_airport_id > airports.airport_id
Ref: flights.arrival_airport_id > airports.airport_id
Ref: tickets.booking_id > bookings.booking_id
