1. installare squid proxy 
    > sudo apt install squid

2. configurare correttamente squid.conf

3. parsare il conf

> sudo squid -k parse

4. avviare il servizio

> systemctl start squid  
> systemctl restart squid  

5. in ogni pc che vuole accedere al webserver:
    - da terminale aggiungere a .bashrc / .zshrc 
        ```bash
            export http_server=100.100.6.3:3128
            export https_server=100.100.6.3:3128
        ```
    - da browser impostare la proxy a `100.100.6.3:3128`
    - 