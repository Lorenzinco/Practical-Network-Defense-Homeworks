# Brainstorming
We decided to create more VPN servers to efficiently divide our addresses into distint subnets to identify the user permissions through their IP Addresses.

The network assigned to the Road Warriors VPN was 100.100.253.0/24, which has been divided into the following subnets:
100.100.253.0/26      for the standard users
100.100.253.64/26    for the power user
100.100.253.128/26   for the administrators.

We also decided to include in the openvpn configuration the IPv6 addresses, which had been configured before on the ACME Network. The resulting subnets are: 
2001:470:b5b8:a00::/64    for the Standard Users
2001:470:b5b8:a01::/64     for the Power Users
2001:470:b5b8:a02::/64    for the Administrators

For the IPsec tunnel, we opted for a route-based implementation to meet the requirement that any packet running between the two routers should go through an IPSec tunnel. This setup involves creating an IPSec tunnel and configuring static routes on both routers to ensure that all the traffic flows through the secure tunnel.


# 27/5

1. Creazione Certification Authority
2. Creazione Certificati VPN Server e Utenti
3. Creazione degli Utenti e assegnazione di password e certificati.
   - `Alice` : `i3c5:6?Q2H,w`
   - `Bob` : `c#<2232YfawZ`
   - `Christina` : `-e>\N3P9r!5£`
4. Creazione Gruppi e assegnazione utenti
   1. Standard_Users - Alice
   2. Power_users - Bob
   3. administrators - Christina
5. Creazione dei server VPN
   1. Certificato TLS su static keys.
   2. Server per Standard Users:
      1. Porta 1336
      2. IPv4 100.100.253.0/26
      3. IPv6 2001:470:b5b8:a00::/64
   3. Server per Power Users:
      1. Porta 1337
      2. IPv4 100.100.253.64/26
      3. IPv6 2001:470:b5b8:a01::/64   
      4. Accesso al DNS
   4. Server per administrator:
      1. Porta 1337
      2. IPv4 100.100.253.128/26
      3. IPv6 2001:470:b5b8:a02::/64   
      4. Accesso al DNS

Abbiamo cambiato per ogni server VPN configurato le impostazioni di cifratura per rendere il flusso più sicuro

# 29/5

- Impostato Alias per i gruppi
- Impostato regole firewall relativi alla VPN
- 
   

# TODO 
1. TEST
2. IPSEC
3. Test IPSEC
