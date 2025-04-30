Main Firewall Router  - 
Internal Firewall Router - 

DMZ - 100.100.6.0/24
- Web Server - webserver.acme-10.test - 100.100.6.2 - fe80::40fa:57ff:fe4a:2073
- Proxy Server - proxyserver.acme-10.test - 100.100.6.3 - fe80::74da:b5ff:fed2:952a

External Services - 100.100.4.0/24
- Client ext 1 - client-ext-1.acme-10.test - 100.100.4.100 - fe80::476a:a47b:68a:a64d
- Fantastic COffee - fantastic-coffee.acme-10.test -  100.100.4.1

INternal Servers Network - 100.100.1.0/24
- Domain Controller (DNS SERVER) - 100.100.1.2
- Log Server - logserver.acme-10.test - 100.100.1.3 - fe80::14cd:d6ff:fe00:4e4c
- GreenBone - greenbone.acme-10.test - 100.100.1.4 - fe80::e03b:f1ff:fef8:8a8c
- Graylog - graylog.acme-10.test - 100.100.1.10 - fe80::8c:10ff:fe8c:c954


Clients Network - 100.100.2.0/24
- Kali (PC) - kali.acme-10.test kali - 100.100.2.100 - fe80::476a:a47b:68a:a64d
- ArpWatch - arpwatch-clients.acme-10.test - 100.100.2.250 - fe80::b89d:d3ff:feec:ea07

monitorserver.acme-10.test
- 100.100.1.254 - fe80::687d:cdff:fe38:29cd
- 100.100.2.254 - fe80::455:36ff:fea8:2642
- 100.100.4.254 - fe80::846:4eff:feb8:bb80
- 100.100.6.254 - fe80::7c8b:8bff:fe15:857e
- 100.100.10.10 - fe80::b459:e3ff:fee0:421a