Table bookings {
  booking_id int [pk, increment]
  guest_id int
  room_id int
}

Ref: bookings.guest_id > guests.guest_id
Ref: bookings.room_id > rooms.room_id
