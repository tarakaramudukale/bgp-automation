# Cisco BGP Network Automation Lab (Python + Netmiko + YAML)

## Overview

This project demonstrates **network automation for Cisco routers** using **Python**, **Netmiko**, and **YAML inventory**.
The script automatically configures **interfaces and BGP neighbors** across multiple routers.

This lab was built and tested using **GNS3**.

---

## Technologies Used

* Python
* Netmiko
* YAML
* Cisco IOS
* GNS3

---

## Network Topology

Routers used in this lab:

R2 (AS 65002)
R3 (AS 65003)
R4 (AS 65004)

BGP peerings:

R2 ↔ R3
R3 ↔ R4
R2 ↔ R1

---

## Project Files

routers.yml
Inventory file containing router IPs, interfaces, ASN, and BGP neighbors.

bgp_automation.py
Python script that reads the YAML file and pushes configuration to routers.

requirements.txt
Python dependencies required for the project.

README.md
Project documentation.

---

## Example YAML Inventory

```
routers:

  R2:
    device_type: cisco_ios
    host: 2.2.2.2
    username: cisco
    password: cisco
    asn: 65002
```

---

## Installation

Install dependencies:

```
pip install -r requirements.txt
```

---

## Run Automation Script

```
python bgp_automation.py
```

The script will:

• Configure router interfaces
• Configure BGP ASN
• Configure BGP neighbors
• Apply configuration automatically

---

## Skills Demonstrated

Network Automation
Python scripting
Cisco BGP configuration
YAML inventory management
Infrastructure automation

---

## Author

Network Automation Lab Project
Built for learning Python Network Automation.
