Table appointments {
  appointment_id int [pk, increment]
  patient_id int
  doctor_id int
  appointment_date datetime
}

Ref: appointments.patient_id > patients.patient_id
Ref: appointments.doctor_id > doctors.doctor_id
