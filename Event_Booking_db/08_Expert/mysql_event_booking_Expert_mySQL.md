Table events {
  event_id int [pk, increment]
  venue_id int
  title varchar(255)
}

Ref: events.venue_id > venues.venue_id
