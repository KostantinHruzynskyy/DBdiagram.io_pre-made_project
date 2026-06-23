Table bookings {
  booking_id int [pk, increment]
  attendee_id int
  ticket_id int
}

Ref: bookings.attendee_id > attendees.attendee_id
Ref: bookings.ticket_id > tickets.ticket_id
