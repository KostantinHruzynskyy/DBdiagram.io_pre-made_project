Table offers {
  offer_id int [pk, increment]
  property_id int
  client_id int
  amount decimal
}

Ref: offers.property_id > properties.property_id
Ref: offers.client_id > clients.client_id
