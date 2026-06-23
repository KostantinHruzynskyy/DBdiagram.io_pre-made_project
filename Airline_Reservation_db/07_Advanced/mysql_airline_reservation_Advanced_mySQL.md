Table tickets {
  ticket_id int [pk, increment]
  booking_id int
  seat_number varchar(10)
}

Ref: tickets.booking_id > bookings.booking_id
