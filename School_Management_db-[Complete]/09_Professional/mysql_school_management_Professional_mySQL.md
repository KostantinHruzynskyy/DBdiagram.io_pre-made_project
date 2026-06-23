Table students {
  student_id int [pk, increment]
  class_id int
  name varchar(255)
  email varchar(255)
}

Table teachers {
  teacher_id int [pk, increment]
  name varchar(255)
}

Table classes {
  class_id int [pk, increment]
  teacher_id int
  name varchar(100)
}

Table subjects {
  subject_id int [pk, increment]
  name varchar(100)
}

Table grades {
  grade_id int [pk, increment]
  student_id int
  subject_id int
  score decimal
}

Table attendance {
  attendance_id int [pk, increment]
  student_id int
  date date
  present boolean
}

Ref: students.class_id > classes.class_id
Ref: classes.teacher_id > teachers.teacher_id
Ref: grades.student_id > students.student_id
Ref: grades.subject_id > subjects.subject_id
Ref: attendance.student_id > students.student_id
