Table payments {
  payment_id int [pk, increment]
  booking_id int
  amount decimal
}

Ref: payments.booking_id > bookings.booking_id
