Table rooms {
  room_id int [pk, increment]
  room_number varchar(20)
  capacity int
}

Table admissions {
  admission_id int [pk, increment]
  patient_id int
  room_id int
}

Ref: admissions.patient_id > patients.patient_id
Ref: admissions.room_id > rooms.room_id
