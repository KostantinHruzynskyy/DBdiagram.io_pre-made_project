Table payments {
  payment_id int [pk, increment]
  ride_id int
  amount decimal
  method varchar(50)
}

Table rides {
  ride_id int [pk, increment]
  status varchar(50)
}

Ref: payments.ride_id > rides.ride_id
