Table tickets {
  ticket_id int [pk, increment]
  event_id int
  price decimal
}

Ref: tickets.event_id > events.event_id
