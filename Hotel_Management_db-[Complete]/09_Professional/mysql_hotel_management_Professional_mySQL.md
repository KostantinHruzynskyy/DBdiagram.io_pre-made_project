Table guests {
  guest_id int [pk, increment]
  name varchar(255)
  email varchar(255)
}

Table rooms {
  room_id int [pk, increment]
  room_number varchar(20)
  room_type varchar(50)
  price_per_night decimal
}

Table bookings {
  booking_id int [pk, increment]
  guest_id int
  room_id int
  check_in date
  check_out date
  status varchar(50)
}

Table payments {
  payment_id int [pk, increment]
  booking_id int
  amount decimal
}

Table services {
  service_id int [pk, increment]
  name varchar(255)
  price decimal
}

Table booking_services {
  id int [pk, increment]
  booking_id int
  service_id int
}

Ref: bookings.guest_id > guests.guest_id
Ref: bookings.room_id > rooms.room_id
Ref: payments.booking_id > bookings.booking_id
Ref: booking_services.booking_id > bookings.booking_id
Ref: booking_services.service_id > services.service_id
