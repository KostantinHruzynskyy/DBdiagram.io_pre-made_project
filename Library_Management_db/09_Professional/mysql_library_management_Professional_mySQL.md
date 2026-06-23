Table authors {
  author_id int [pk, increment]
  name varchar(255)
}

Table publishers {
  publisher_id int [pk, increment]
  name varchar(255)
}

Table books {
  book_id int [pk, increment]
  author_id int
  publisher_id int
  title varchar(255)
  isbn varchar(20)
}

Table members {
  member_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table loans {
  loan_id int [pk, increment]
  member_id int
  book_id int
  loan_date date
  return_date date
}

Table fines {
  fine_id int [pk, increment]
  loan_id int
  amount decimal
}

Ref: books.author_id > authors.author_id
Ref: books.publisher_id > publishers.publisher_id
Ref: loans.member_id > members.member_id
Ref: loans.book_id > books.book_id
Ref: fines.loan_id > loans.loan_id
