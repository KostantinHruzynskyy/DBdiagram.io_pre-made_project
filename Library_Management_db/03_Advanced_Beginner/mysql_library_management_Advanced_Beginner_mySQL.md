Table authors {
  author_id int [pk, increment]
  name varchar(255)
}

Table books {
  book_id int [pk, increment]
  author_id int
  title varchar(255)
}

Ref: books.author_id > authors.author_id
