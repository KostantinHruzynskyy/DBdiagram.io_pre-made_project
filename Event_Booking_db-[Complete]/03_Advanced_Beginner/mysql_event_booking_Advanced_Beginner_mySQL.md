Table organizers {
  organizer_id int [pk, increment]
  name varchar(255)
}

Table events {
  event_id int [pk, increment]
  organizer_id int
  title varchar(255)
}

Ref: events.organizer_id > organizers.organizer_id
