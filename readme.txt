# nasledujici prikaz podepisuje Honzuv hlasovaci listek  - v linux-u je openssl uz nainstalovano
openssl dgst -sha256 -sign priv.pem -out ticket.txt.sha256 Jan_ticket.txt

# nasledujici prikaz overuje podpis (ticket.txt.sha256) Honzuv hlasovaci listek
openssl dgst -sha256 -verify Jan_pub.pem -signature ticket.txt.sha256 Jan_ticket.txt
