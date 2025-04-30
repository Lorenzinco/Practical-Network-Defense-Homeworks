1. DNS - avoid resetting of RESOLV.conf
> touch /etc/.pve-ignore.resolv.conf

2. restart DNS server service
> systemctl restart dnsmasq.service

## DNS CONFIG:

- file /etc/hosts in the dns server as in this folder
- file /etc/resolv.conf as in this folder for every host using the dns server in the ACME network