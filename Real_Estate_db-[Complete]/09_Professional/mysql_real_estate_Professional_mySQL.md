Table agents {
  agent_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table properties {
  property_id int [pk, increment]
  agent_id int
  title varchar(255)
  description text
  price decimal
}

Table clients {
  client_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table viewings {
  viewing_id int [pk, increment]
  property_id int
  client_id int
  viewing_date date
}

Table offers {
  offer_id int [pk, increment]
  property_id int
  client_id int
  amount decimal
  status varchar(50)
}

Table contracts {
  contract_id int [pk, increment]
  offer_id int
  signed_date date
}

Ref: properties.agent_id > agents.agent_id
Ref: viewings.property_id > properties.property_id
Ref: viewings.client_id > clients.client_id
Ref: offers.property_id > properties.property_id
Ref: offers.client_id > clients.client_id
Ref: contracts.offer_id > offers.offer_id
