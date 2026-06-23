Table doctors {
  doctor_id int [pk, increment]
  name varchar(255)
  specialization varchar(255)
}

Table patients {
  patient_id int [pk, increment]
  name varchar(255)
}
