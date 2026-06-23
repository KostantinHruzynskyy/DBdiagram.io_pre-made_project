Table classes {
  class_id int [pk, increment]
  name varchar(100)
}

Table students {
  student_id int [pk, increment]
  class_id int
  name varchar(255)
}

Ref: students.class_id > classes.class_id
