Table interviews {
  interview_id int [pk, increment]
  application_id int
  interview_date datetime
}

Ref: interviews.application_id > applications.application_id
