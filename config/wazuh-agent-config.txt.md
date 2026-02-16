Wazuh Agent installed on Windows 10 endpoint using MSI installer.

Agent registered with Wazuh Manager running on Ubuntu Server.



"C:\\Program Files (x86)\\ossec-agent\\agent-auth.exe" -m **agent-auth.exe -m 192.168.56.101

net stop wazuhsvc**

**net start wazuhsvc

sc query wazuhsvc**

<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>


====================================================
Wazuh Agent Configuration (Windows 10 Endpoint)
====================================================

Project Component:
- Windows 10 monitored endpoint machine
- Wazuh Agent installed and connected to Wazuh Manager
- Sysmon integrated for advanced event logging

----------------------------------------------------
1. Agent Authentication with Wazuh Manager
----------------------------------------------------

The Windows agent was registered with the Ubuntu-based
Wazuh Manager using the agent-auth utility:

Command:

agent-auth.exe -m <WAZUH-MANAGER-IP>

Example (Lab Network):

agent-auth.exe -m 192.168.56.101

----------------------------------------------------
2. Restarting the Wazuh Agent Service (Windows)
----------------------------------------------------

After updating configuration files, the agent service
was restarted using:

net stop wazuhsvc
net start wazuhsvc

Alternative (PowerShell):

Restart-Service wazuhsvc

----------------------------------------------------
3. Sysmon EventChannel Integration (ossec.conf)
----------------------------------------------------

Sysmon logs were collected through Windows EventChannel
by adding the following snippet inside ossec.conf:

<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>

This enables Wazuh to ingest Sysmon Operational logs
for threat detection and alert generation.

----------------------------------------------------
4. Service Verification
----------------------------------------------------

To confirm the agent is running:

sc query wazuhsvc

====================================================
End of Agent Configuration Notes
====================================================