# Notes HW1

Group 10

Tommaso De Nicola - 2006686  
Lorenzo Colombini - 1973692  
Mattia Romano - 1982886  

# Initial Brainstorming
We initially decided to complete every step of the assignment following the order given by the professor. 
Initially we decided not to implement IPv6 Rules on Firewalls because it wasn't clearly requested and because all the requests can be implemented through only IPv4.

## 24/04
1. brainstorming about functioning of ProxMox interface and about what to do
2. verified how to download configuration file of firewalls using the vpn connection
3. modified the main-firewall following the instruction on the assignment, through the client-ext (connecting to 100.100.4.1)
   - unticked the 2 options in Interfaces -> [WAN] -> block private / bogon networks
   - mantained the pass rule for ICMP packets for every host
   - inserted a rule tu consent HTTP packets on 80 towards the DMZ from the 100.101.0.0/24 network
  
## 26/04
### All the ACME hosts must use the internal DNS Server as a DNS resolver
1. edited the /etc/resolv.conf file in every host in order to
2. installed dnsmasq on dns server
3. inserted on hosts file of dns server all the entries
4. tested the DNS -> IT WORKS!

### Regole Firewall per DNS
1. creato nuovo gruppo di interfacce -> ACME -> tutti le interfacce interne della nostra infra
2. creata regola (float) per i pacchetti DNS all'interno della acme network su entrambi i firewall
