Table groups {
  group_id int [pk, increment]
  name varchar(255)
}

Table group_members {
  group_id int
  user_id int
}

Ref: group_members.group_id > groups.group_id
Ref: group_members.user_id > users.user_id
