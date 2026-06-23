Table users {
  user_id int [pk, increment]
  email varchar(255)
}

Table profiles {
  profile_id int [pk, increment]
  user_id int
  name varchar(255)
}

Table movies {
  movie_id int [pk, increment]
  title varchar(255)
  language varchar(50)
}

Table watch_events {
  id int [pk, increment]
  profile_id int
  movie_id int
  progress int
}

Ref: profiles.user_id > users.user_id
Ref: watch_events.profile_id > profiles.profile_id
Ref: watch_events.movie_id > movies.movie_id