Table categories {
  category_id int [pk, increment]
  name varchar(100)
}

Table products {
  product_id int [pk, increment]
  name varchar(255)
  category_id int
}

Ref: products.category_id > categories.category_id
