Table users {
  user_id int [pk, increment]
  name varchar(255)
}

Table properties {
  property_id int [pk, increment]
  owner_id int
}

Ref: properties.owner_id > users.user_id