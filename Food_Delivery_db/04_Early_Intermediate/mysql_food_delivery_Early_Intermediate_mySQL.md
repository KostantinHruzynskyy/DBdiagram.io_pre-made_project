Table menu_items {
  item_id int [pk, increment]
  restaurant_id int
  name varchar(255)
  price decimal
}

Ref: menu_items.restaurant_id > restaurants.restaurant_id
