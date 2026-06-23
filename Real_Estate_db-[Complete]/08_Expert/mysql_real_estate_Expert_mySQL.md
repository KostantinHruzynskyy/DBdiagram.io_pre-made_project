Table property_images {
  image_id int [pk, increment]
  property_id int
  image_url varchar(500)
}

Ref: property_images.property_id > properties.property_id
