Table medical_records {
  record_id int [pk, increment]
  patient_id int
  diagnosis text
  created_at timestamp
}

Ref: medical_records.patient_id > patients.patient_id
