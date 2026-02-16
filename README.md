# Wazuh-SIEM-Lab
VirtualBox SIEM Lab using Wazuh + Sysmon with simulated attack alerts.

# Wazuh SIEM Threat Detection Lab (Sysmon + VirtualBox)

This repository contains a complete **SIEM-based Threat Detection and Endpoint Monitoring Lab** built using **Wazuh** and **Sysmon** inside a virtualized environment.

The project demonstrates how endpoint telemetry from a Windows machine can be collected, analyzed, and visualized through Wazuh dashboards to detect suspicious activity mapped to the **MITRE ATT&CK framework**.

---

## 📌 Project Overview

The objective of this project was to design and implement a SOC-style monitoring lab capable of:

- Collecting detailed Windows security logs using **Sysmon**
- Forwarding telemetry using the **Wazuh Agent**
- Centralizing analysis through the **Wazuh Manager**
- Simulating attacker behavior in a controlled environment
- Generating alerts and visualizing detections in the Wazuh Dashboard

This lab provides hands-on experience in SIEM deployment, endpoint detection, and threat monitoring workflows.

---

## 🏗️ Lab Architecture

<img width="1024" height="1024" alt="architecture" src="https://github.com/user-attachments/assets/5378e08a-e92b-462b-a999-12cd26dabd36" />


**Log and Detection Flow:**

Kali Linux (Attacker Simulation)  
→ Windows 10 Endpoint (Sysmon + Wazuh Agent)  
→ Ubuntu Server (Wazuh Manager + Dashboard)  
→ Alerts + MITRE ATT&CK Mapping

---

## ⚙️ Environment Setup

This project was deployed using **Oracle VirtualBox** with the following virtual machines:

| Machine | Operating System | Role |
|--------|------------------|------|
| SIEM Server | Ubuntu Server | Wazuh Manager + Dashboard |
| Endpoint Machine | Windows 10 | Sysmon + Wazuh Agent |
| Attacker Machine | Kali Linux | Attack Simulation |

---

## 🔧 Tools & Technologies Used

- **Wazuh SIEM**
- **Sysmon (System Monitor)**
- **MITRE ATT&CK Framework**
- **Oracle VirtualBox**
- Windows Event Logging (EventChannel)
- Kali Linux security utilities

---

## 🔥 Key Features Implemented

- Installed and configured Wazuh Manager on Ubuntu Server  
- Integrated Windows 10 endpoint using Wazuh Agent  
- Enabled Sysmon logging for high-fidelity endpoint telemetry  
- Forwarded Sysmon Operational logs to Wazuh via EventChannel  
- Simulated suspicious activity from Kali Linux  
- Successfully generated and visualized alerts including:

  - PowerShell execution behavior  
  - Suspicious process creation  
  - Executable drops in malware-associated paths  
  - Authentication-related security events  
  - MITRE ATT&CK technique mapping  

---

## 🛡️ Detection Results

The Wazuh Dashboard successfully displayed security alerts generated from Sysmon telemetry.

Examples of detected behaviors:

- Suspicious PowerShell spawning activity  
- Discovery and reconnaissance commands  
- Malware-like executable drop locations  
- Endpoint security anomalies

Alerts were observable through:

- **Security Events Dashboard**
- **Alert Timeline View**
- **MITRE ATT&CK Mapping Panel**

---

## 📷 Project Screenshots

### Virtual Lab Environment Setup

<img width="1919" height="1022" alt="Virtual Lab Setup in Oracle VirtualBox" src="https://github.com/user-attachments/assets/56dc211f-89d5-4d73-b181-59f9aeeb75f8" />

### Wazuh Security Dashboard Overview

<img width="1920" height="918" alt="Wazuh Dashboard Overview (48 Events)" src="https://github.com/user-attachments/assets/7f90e440-8715-41be-b91e-8a622de0cf83" />
<img width="1920" height="912" alt="Wazuh Dashboard Overview (406 Events Spike)" src="https://github.com/user-attachments/assets/6e7f9c8b-c358-476e-9134-5ad32ef798c2" />

### Alerts Generated from Sysmon Events
<img width="1920" height="962" alt="Wazuh Events Timeline + Alert Hits" src="https://github.com/user-attachments/assets/a024f34c-b9c8-46f5-be7b-5a370f0ba0c7" />


### Security Alerts Table with MITRE ATT&CK Mapping
<img width="1920" height="910" alt="Security Alerts Table (MITRE Mapping View)" src="https://github.com/user-attachments/assets/0d8f21fd-74e4-4cf8-89cf-ea3163183791" />


---

## 📂 Repository Structure
Wazuh-SIEM-Lab/
├── screenshots/
├── flowchart/
├── configs/
└── notes/


---

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- SIEM deployment and configuration  
- Endpoint monitoring using Sysmon  
- Centralized log collection and correlation with Wazuh  
- SOC-style alert investigation workflows  
- MITRE ATT&CK based threat detection mapping  
- Building cybersecurity labs in isolated virtual environments  

---

## 🚀 Future Improvements

Potential enhancements to extend this project:

- Writing custom Wazuh detection rules  
- Adding automated active response actions  
- Integrating Suricata for network-based IDS  
- Expanding the lab to multiple monitored endpoints  
- Simulating additional attack techniques (persistence, lateral movement)

---

## ⚠️ Ethical Note

All simulations and detections were performed **only inside an isolated Oracle VirtualBox lab environment**.  
No real-world systems were targeted.

---

## 📌 Conclusion

This project demonstrates a complete working SIEM + endpoint monitoring lab using **Wazuh and Sysmon**, capable of detecting suspicious attacker-like behavior and visualizing alerts through a SOC-style dashboard.

It serves as a strong foundation for advanced cybersecurity monitoring, intrusion detection research, and SIEM engineering practices.

---



