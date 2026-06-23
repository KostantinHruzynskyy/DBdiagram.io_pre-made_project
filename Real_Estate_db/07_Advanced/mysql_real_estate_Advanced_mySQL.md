Table contracts {
  contract_id int [pk, increment]
  offer_id int
  signed_date date
}

Ref: contracts.offer_id > offers.offer_id
