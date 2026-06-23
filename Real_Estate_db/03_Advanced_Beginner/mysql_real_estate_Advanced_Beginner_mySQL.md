Table agents {
  agent_id int [pk, increment]
  name varchar(255)
}

Table properties {
  property_id int [pk, increment]
  agent_id int
  title varchar(255)
}

Ref: properties.agent_id > agents.agent_id
