Table companies {
  company_id int [pk, increment]
  name varchar(255)
}

Table jobs {
  job_id int [pk, increment]
  company_id int
  title varchar(255)
  location varchar(255)
}

Table candidates {
  candidate_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table resumes {
  resume_id int [pk, increment]
  candidate_id int
  file_url varchar(500)
}

Table applications {
  application_id int [pk, increment]
  candidate_id int
  job_id int
  status varchar(50)
}

Table interviews {
  interview_id int [pk, increment]
  application_id int
  interview_date datetime
}

Ref: jobs.company_id > companies.company_id
Ref: resumes.candidate_id > candidates.candidate_id
Ref: applications.candidate_id > candidates.candidate_id
Ref: applications.job_id > jobs.job_id
Ref: interviews.application_id > applications.application_id
