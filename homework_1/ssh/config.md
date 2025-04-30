1. verificare che tutti gli host abbiano il servizio ssh running: `service ssh status`
   - arpwatch-clients V
   - dnsserver      V (enabled it but it wasn't up)
   - logserver      V
   - monitorserver  V
   - greenbone      X
   - webserver      V
   - proxyserver    V (enabled it but it wasn't up)
   - fantastic-coffee   ???
   - graylog        V (enabled it but it wasn't up)

2. connettersi ad un server con ssh attivo da uno dei client (arpwatch-clients / kali)
   1. arpwatch ha la key generata per il log server, e già inserita

3. copiare la chiava pubblica nel file authorized_keys del server a cui connettersi

4. connettersi in ssh  
