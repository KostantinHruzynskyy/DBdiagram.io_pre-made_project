Table branches {
  branch_id int [pk, increment]
  name varchar(255)
  location varchar(255)
}

Table accounts {
  account_id int [pk, increment]
  branch_id int
  balance decimal
}

Ref: accounts.branch_id > branches.branch_id
