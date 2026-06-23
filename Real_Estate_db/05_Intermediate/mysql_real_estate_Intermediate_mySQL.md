Table viewings {
  viewing_id int [pk, increment]
  property_id int
  client_id int
  viewing_date date
}

Ref: viewings.property_id > properties.property_id
Ref: viewings.client_id > clients.client_id
