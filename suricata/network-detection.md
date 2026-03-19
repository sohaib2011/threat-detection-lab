# Network Intrusion Detection (NIDS)

We have already installed suricata as of peravious work of (bare is noe bs at vi har gjort det før). To check (basically vi starter og sjekker tjeneste)

<img width="773" height="275" alt="image" src="https://github.com/user-attachments/assets/33ce99d3-8ab7-4b35-862b-516ca7f0daa3" />


<img width="513" height="83" alt="image" src="https://github.com/user-attachments/assets/4d61f91e-e5e3-4067-b9de-4a0db415e460" /> (bilde av sudo tail -f /var/log/suricata/fast.log)

Nice! There are no current logs running as of now, so we can add a new custom rule

<img width="377" height="63" alt="image" src="https://github.com/user-attachments/assets/81607b70-3ecc-49b8-8a62-daab162f3a93" />

In /etc/suricata/rules directory, create a new file called local.rules. This is where we will lage ny regler lalla

<img width="377" height="63" alt="image" src="https://github.com/user-attachments/assets/e93c5b9b-f58a-4baf-a3a0-9c432328a37d" /> (bilde av suricata directory nano greia)

Our suricata rule will be simple, we want an alert to basically icmp requests (ping)

``bash 
alert icmp any any -> any any (msg:"ICMP Ping detected"; sid:1000001; rev:1;)


Since this file was constructed by us, we  need to add file local.rule in .yaml file, and change the default-rule path to /etc/suricata/rules

<img width="547" height="234" alt="image" src="https://github.com/user-attachments/assets/857a11ca-b275-4884-b4ee-938129f59ee5" /> 


<img width="1259" height="281" alt="image" src="https://github.com/user-attachments/assets/c4b14c3e-8d3c-47c7-8f18-c10a0372271b" />

We want to verify, alles gute! Just restart the suricata with systemctl SUDO restart suricata and we good


Now to test if NIDS working, we will probe the alert
<img width="681" height="693" alt="image" src="https://github.com/user-attachments/assets/cc49b152-90d5-4df6-8fa3-fa0db5fa983a" /> (commands)


<img width="1696" height="142" alt="image" src="https://github.com/user-attachments/assets/5ac12351-55f8-4914-b1d8-c83f75aca992" /> (resultat av skannet)

si den er litt treig og tar tid på registrere men hey vi klarte
