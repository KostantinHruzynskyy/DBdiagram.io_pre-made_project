Table baggage {
  baggage_id int [pk, increment]
  ticket_id int
  weight_kg decimal
}

Ref: baggage.ticket_id > tickets.ticket_id
