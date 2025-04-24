# Notes HW1

Group: ACME-10

## 24/04
1. brainstorming about functioning of ProxMox interface and about what to do
2. verified how to download configuration file of firewalls using the vpn connection
3. modified the main-firewall following the instruction on the assignment, through the client-ext (connecting to 100.100.4.1)
   - unticked the 2 options in Interfaces -> [WAN] -> block private / bogon networks
   - mantained the pass rule for ICMP packets for every host
   - inserted a rule tu consent HTTP packets on 80 towards the DMZ from the 100.101.0.0/24 network
