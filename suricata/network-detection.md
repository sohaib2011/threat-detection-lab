# Network Intrusion Detection (NIDS)

We have already installed Suricata in earlier works in kali, so the installation process wil not be included. This step will focus on verifing that the suricata service is running correctly instead

![image](https://github.com/user-attachments/assets/33ce99d3-8ab7-4b35-862b-516ca7f0daa3)

Service has started successfully as seen in the field saying "active"


![image](https://github.com/user-attachments/assets/4d61f91e-e5e3-4067-b9de-4a0db415e460)

Nice! There are no current logs running as of now, which means no alerts have been triggered. We can proceed with adding a new custom rule


![image](https://github.com/user-attachments/assets/81607b70-3ecc-49b8-8a62-daab162f3a93)

In /etc/suricata/rules directory, create a new file called local.rules. This file will be used to define personalised detection rules 

![image](https://github.com/user-attachments/assets/e93c5b9b-f58a-4baf-a3a0-9c432328a37d)


Our Suricata rule will be simple. We want to generate an alert for ICMP requests (ping traffic):

```bash
alert icmp any any -> any any (msg:"ICMP Ping detected"; sid:1000001; rev:1;)
```


![image](https://github.com/user-attachments/assets/857a11ca-b275-4884-b4ee-938129f59ee5)

To ensure that suricata loads up our custom rule, we need to update the config file (suricata.yaml). This can be done by setting default-rule path to /etc/suricata/rules and adding local rules under rule-files

```yaml
default-rule-path: /etc/suricata/rules

rule-files:
  - local.rules
```

![image](https://github.com/user-attachments/assets/c4b14c3e-8d3c-47c7-8f18-c10a0372271b)

Everything looks good, so we just restart the Suricata service using:


## NIDS testing

Now to test if NIDS working, we will probe the alert

![image](https://github.com/user-attachments/assets/cc49b152-90d5-4df6-8fa3-fa0db5fa983a)


![image](https://github.com/user-attachments/assets/5ac12351-55f8-4914-b1d8-c83f75aca992)

It is a bit slow and takes some time to register, but hey we got it working.
