Table departments {
  department_id int [pk, increment]
  name varchar(255)
}

Table doctors {
  doctor_id int [pk, increment]
  department_id int
  name varchar(255)
}

Ref: doctors.department_id > departments.department_id
