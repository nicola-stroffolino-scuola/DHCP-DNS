# DHCP-DNS

Tramite il subnetting a 4 abbiamo diviso una rete, la quale subnet è `255.255.255.0` e che permette l'entrata di 254 host, in 4 sottoreti la quale ognuna permette l'entrata di 64 host.

Le 4 sottoreti :
+ **172.130.20.0** $\rightarrow$ Avrà come range di host `172.130.20.1` a `172.130.20.62` dove `172.130.20.63` sarà utilizzato come broadcast.
+ **172.130.20.64** $\rightarrow$ Avrà come range di host `172.130.20.65` a `172.130.20.126` dove `172.130.20.127` sarà utilizzato come broadcast.
+ **172.130.20.128** $\rightarrow$ Avrà come range di host `172.130.20.129` a `172.130.20.190` dove `172.130.20.191` sarà utilizzato come broadcast.
+ **172.130.20.192** $\rightarrow$ Avrà come range di host `172.130.20.193` a `172.130.20.253` dove `172.130.20.254` sarà utilizzato come broadcast.

Per ogni sottorete abbiamo impostato un server DHCP che inizia a distribuire gli IP nei range elencati precendemente.
Nella sottorete `172.130.20.128` abbiamo inserito un server HTTP che ha lo scopo di mantenere attiva una pagina WEB all'indirizzo `SIRulez.it`; nella stessa sottorete abbiamo anche impostato un server DNS che associerà il dominio pagina WEB `SIRulez.it` al suo indirizzo IP.

I server DHCP, HTTP e DNS sono configurati staticamente.
