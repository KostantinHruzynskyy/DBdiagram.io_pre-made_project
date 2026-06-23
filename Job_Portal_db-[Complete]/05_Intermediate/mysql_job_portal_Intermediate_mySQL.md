Table applications {
  application_id int [pk, increment]
  candidate_id int
  job_id int
}

Ref: applications.candidate_id > candidates.candidate_id
Ref: applications.job_id > jobs.job_id
