Table patients {
  patient_id int [pk, increment]
  name varchar(255)
  birth_date date
  email varchar(255)
}

Table departments {
  department_id int [pk, increment]
  name varchar(255)
}

Table doctors {
  doctor_id int [pk, increment]
  department_id int
  name varchar(255)
  specialization varchar(255)
}

Table appointments {
  appointment_id int [pk, increment]
  patient_id int
  doctor_id int
  appointment_date datetime
  status varchar(50)
}

Table medical_records {
  record_id int [pk, increment]
  patient_id int
  diagnosis text
}

Table prescriptions {
  prescription_id int [pk, increment]
  patient_id int
  doctor_id int
  medication varchar(255)
}

Ref: doctors.department_id > departments.department_id
Ref: appointments.patient_id > patients.patient_id
Ref: appointments.doctor_id > doctors.doctor_id
Ref: medical_records.patient_id > patients.patient_id
Ref: prescriptions.patient_id > patients.patient_id
Ref: prescriptions.doctor_id > doctors.doctor_id
