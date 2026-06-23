Table organizers {
  organizer_id int [pk, increment]
  name varchar(255)
}

Table venues {
  venue_id int [pk, increment]
  name varchar(255)
  city varchar(255)
}

Table events {
  event_id int [pk, increment]
  organizer_id int
  venue_id int
  title varchar(255)
  event_date datetime
}

Table attendees {
  attendee_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table tickets {
  ticket_id int [pk, increment]
  event_id int
  price decimal
}

Table bookings {
  booking_id int [pk, increment]
  attendee_id int
  ticket_id int
}

Ref: events.organizer_id > organizers.organizer_id
Ref: events.venue_id > venues.venue_id
Ref: tickets.event_id > events.event_id
Ref: bookings.attendee_id > attendees.attendee_id
Ref: bookings.ticket_id > tickets.ticket_id
