Table amenities {
  id int [pk, increment]
  name varchar(100)
}

Table property_amenities {
  id int [pk, increment]
  property_id int
  amenity_id int
}