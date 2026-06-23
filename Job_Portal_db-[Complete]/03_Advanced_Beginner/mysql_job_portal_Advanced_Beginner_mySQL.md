Table companies {
  company_id int [pk, increment]
  name varchar(255)
}

Table jobs {
  job_id int [pk, increment]
  company_id int
  title varchar(255)
}

Ref: jobs.company_id > companies.company_id
