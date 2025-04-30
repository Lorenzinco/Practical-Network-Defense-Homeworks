# SUI CLIENT

1. appendere in ogni host la seguente riga in fondo al file /etc/rsyslog.conf:

> *.* @graylog:1514
> *.* @logserver:514

2. verificare che /etc/resolv.conf sia corretto
3. riavviare il servizio di logging
4. creare il file .pve-ignore.rsyslog.conf

# SU GRAYLOG

1. reimpostato la password e l'username a admin:admin
2. riavviato il servizio con systemctl restart graylog.service
3. avviato un input di ascolto in syslog UDP sulla rete locale

# SU logserver

1. impostato un nuovo percorso per loggare i file provenienti dalla rete modificando /etc/rsyslog.conf

> :fromhost-ip, !isequal, "127.0.0.1" /var/log/network_sources.log

2. Decommentato le righe per mettersi in ascolto di traffico UDP sulla porta 514:

> # Provides UDP syslog reception
> module(load="imudp")
> input(type="imudp" port="514")
> 

3. riavviato il servizio


