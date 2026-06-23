Table prescriptions {
  prescription_id int [pk, increment]
  patient_id int
  doctor_id int
  medication varchar(255)
}

Ref: prescriptions.patient_id > patients.patient_id
Ref: prescriptions.doctor_id > doctors.doctor_id
