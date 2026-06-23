Table skills {
  skill_id int [pk, increment]
  name varchar(100)
}

Table candidate_skills {
  candidate_id int
  skill_id int
}

Ref: candidate_skills.candidate_id > candidates.candidate_id
Ref: candidate_skills.skill_id > skills.skill_id
