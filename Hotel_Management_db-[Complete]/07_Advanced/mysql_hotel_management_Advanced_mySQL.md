Table booking_services {
  id int [pk, increment]
  booking_id int
  service_id int
}

Ref: booking_services.booking_id > bookings.booking_id
Ref: booking_services.service_id > services.service_id
