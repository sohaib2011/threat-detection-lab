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


Since this file was constructed by us, we  need to add file local.rule in .yaml file

<img width="584" height="313" alt="image" src="https://github.com/user-attachments/assets/228461a5-7462-4742-bc18-27b5c8d008cb" /> (pic of nano file, where i added local.rule)



