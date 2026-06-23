Table resumes {
  resume_id int [pk, increment]
  candidate_id int
  file_url varchar(500)
}

Ref: resumes.candidate_id > candidates.candidate_id
