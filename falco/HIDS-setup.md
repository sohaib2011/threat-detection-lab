# Host-Based Intrusion Detection System (HIDS) - Falco

For this demo, Falco is already installed and configured, so the installation process is not included.


## Verification

### Check Falco Version

<img width="618" height="112" alt="image" src="https://github.com/user-attachments/assets/cf153a89-f256-4d87-a1b5-4d1553fed7fc" />

Check the falco version to check if its installed, and it follows the newest patch

### Check Service Status

<img width="637" height="145" alt="image" src="https://github.com/user-attachments/assets/d2e45d24-271f-45a6-976f-e8a4857dcf17" />

Verify that Falco Service is active and running

---


## Configuration

<img width="601" height="63" alt="image" src="https://github.com/user-attachments/assets/edf4f663-c15f-4fd4-9634-d0853fc2fcb3" />

 We want to add custom detection rules in Falco, so we need to edit the configuration files located in /etc/falco

<img width="446" height="505" alt="image" src="https://github.com/user-attachments/assets/a5b535d3-cdd1-4bc5-b000-6087c3dea467" />

Here, change falco_rules.local.yaml to load our custom rules. The ruleset defined is already pre-written and included in the repository falco.rules
---

### Apply Changes

<img width="598" height="355" alt="image" src="https://github.com/user-attachments/assets/49ac2f4b-86c3-4f87-9c32-1c3fd2f66b56" />

When done, restart the Falco service and verify its status again to ensure that the new rules are loaded and functioning correctly

---

## Detection Testing


<img width="606" src="https://github.com/user-attachments/assets/743f213c-ce7f-4a99-8399-994d6507539e" />

The monitoring is working! As of now, Falco is capturing all system activity so its scrambled in a huge amount of junk events. To better demonstrate its functionality, lets try to execute malicious commands

---

### Nmap

<img width="623" src="https://github.com/user-attachments/assets/8930b24c-5fd3-4c85-8090-4cea1e21338f" />

Falco detects Nmap as a process, showing full visibility of any malicious attempt. The warning message also clearly stands out from normal activity, making suspicious behavior easy to identify!

---

### Curl

<img width="687" src="https://github.com/user-attachments/assets/c0a9de7c-625d-42ca-a3a3-a9f6d4ebec78" />

Curl activity was detected

---

### Netcat

<img width="605" src="https://github.com/user-attachments/assets/1019694c-5f72-49a5-b424-5982420bfdd9" />

Even netcat wow

---
