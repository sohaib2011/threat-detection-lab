<img width="601" height="63" alt="image" src="https://github.com/user-attachments/assets/e63a8040-7834-45aa-96e0-3bed6f865b62" /># Endpoint & Network Detection Lab

As for this demonstration, i ahve already installed and configured flaco so this is not ... 

<img width="618" height="112" alt="image" src="https://github.com/user-attachments/assets/cf153a89-f256-4d87-a1b5-4d1553fed7fc" />

Verify the version of falco. 

<img width="637" height="145" alt="image" src="https://github.com/user-attachments/assets/d2e45d24-271f-45a6-976f-e8a4857dcf17" />

Check if falco is active as service


1. We want to configure a rule to falco to .... This can be located in /etc/falco

<img width="601" height="63" alt="image" src="https://github.com/user-attachments/assets/edf4f663-c15f-4fd4-9634-d0853fc2fcb3" />

2.  Change configuraiton file in sudo nano /etc/falco/falco_rules.loacl.yaml so we can rule ... . The ruleset is in a seperate file falco.rules

<img width="646" height="505" alt="image" src="https://github.com/user-attachments/assets/a5b535d3-cdd1-4bc5-b000-6087c3dea467" /> (dette er selve nano bilde, bare viste det)

<img width="798" height="355" alt="image" src="https://github.com/user-attachments/assets/49ac2f4b-86c3-4f87-9c32-1c3fd2f66b56" /> (dette er bildet for version stauts


When done restart the falco service, and check status


<img width="1006" height="519" alt="image" src="https://github.com/user-attachments/assets/743f213c-ce7f-4a99-8399-994d6507539e" />
Monitoring is a success! Right now its monitoring everything so its all scrambled random junk. Lets try to use malicious commands...

<img width="1023" height="507" alt="image" src="https://github.com/user-attachments/assets/8930b24c-5fd3-4c85-8090-4cea1e21338f" />
Finding shows nmap scan warning sign yeyeyey


<img width="987" height="83" alt="image" src="https://github.com/user-attachments/assets/c0a9de7c-625d-42ca-a3a3-a9f6d4ebec78" />

Curl command

<img width="1005" height="131" alt="image" src="https://github.com/user-attachments/assets/1019694c-5f72-49a5-b424-5982420bfdd9" />

NETCAT




