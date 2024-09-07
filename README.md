## Objective

To develop and configure a comprehensive Security Operations Center automation environment, integrating Wazuh instance for Security Information and Event Management, Shuffle for Security Orchestration Automation and Response, and TheHive for case management. The project aims to build a functional cybersecurity lab, visualize data flow, automate incident response and prepare for real-world cybersecurity scenarios.

### Skills Learned

- Installation and Configuration
  - Installation of Sysmon on Windows 10 client, Wazuh, Shuffle and TheHive
  - Troubleshooting of installation, setup and configuration issues

- Server Configuration and Connectivity
  - Configuring Wazuh, Shuffle, and TheHive
  - Connecting Windows 10 client to Wazuh and verifying service status

- Telemetry Ingestion and Threat Detection
  - Configuring telemetry ingestion from Windows 10 client to Wazuh
  - Setting up Sysmon and editing configuration files for log collection
  - Creating custom alerts and managing detection for specific threats (e.g., Mimikatz)
  - Restarting services and verifying alert functionality

- Integration and Automation
  - Integrating Wazuh, TheHive and Shuffle for automated incident response
  - Automating alerts and notifications to analysts thru Email
  - Utilizing VirusTotal for hash and IP address reputation checks
  - Configuring TheHive for case management

### Tools Used

- AWS EC2. Provides scalable computing capacity for applications and workloads. It is utilized for hosting servers.
- Wazuh. Offers security visibility into endpoints by monitoring their behavior and identifying threats, vulnerabilities, and anomalies.
- TheHive. A versatile security incident response tool, simplifies the creation, management, and analysis of security incidents.
- Shuffle. Automation for Security Orchestration Automation and Response.
- VirusTotal. Analyzes suspicious files, hash, IP address for malware and malicious content using antivirus engines and website scanners.
- Email. Used to send notifications to analysts, prompting them to investigate incidents further.
- Sysmon. Track and record system activity in the Windows event log.

## Lab Information

<p align="center">
<img src="https://imgur.com/6HEYBN2.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Network Diagram</b>
<br/>

<p align="center">
<img src="https://imgur.com/wivv3MM.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Workflow</b>
<br/>

### Lab Hosts

- AWS EC2 Instance
  - Ubuntu 22.04 LTS
    - Wazuh
    - TheHive
    - Shuffle
- Windows 10 Eval
  - Simulates employee workstation
  - Sysmon  
  - Wazuh agent (Forwards Sysmon logs)
- Ubuntu 22.04 LTS
  - On-prem server
  - Wazuh agent
  - SSH server installed
  - IP Address : 192.168.0.204

- Attacker's machine
  - Perform SSH bruteforce attack using Hydra.
  - IP Address : 192.168.0.202

- Checking network connectivity on hosts
<p align="center">
<img src="https://imgur.com/YYx7MqU.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>AWS EC2 Instace state are running</b>
<br/>

<p align="center">
<img src="https://imgur.com/2RL3LMR.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Wazuh Manager dashboards agents status</b>
<br/>

<p align="center">
<img src="https://imgur.com/vIrIMux.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Windows 10 client connectivity with the Wazuh Manager</b>
<br/>

<p align="center">
<img src="https://imgur.com/fJbOWjx.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Ubuntu server connectivity with the Wazuh Manager</b>
<br/>

<p align="center">
<img src="https://imgur.com/dtfeFsU.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>TheHive is running</b>
<br/>

<p align="center">
<img src="https://imgur.com/3omDcHi.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle for Windows 10 client</b>
<br/>

<p align="center">
<img src="https://imgur.com/Bywe63L.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle for Ubuntu server</b>
<br/>

- Generate traffic
<p align="center">
<img src="https://imgur.com/IQw0LYs.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Windows client Mimikatz was executed</b>
<br/>

<p align="center">
<img src="https://imgur.com/PwVRl9y.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Attacker's machine SSH brute-force attack</b>
<br/>

- Server ingestion, analysis, alerts and response
<p align="center">
<img src="https://imgur.com/FSCN2wU.png" height="40%" width="40%" alt="Device Specification"/>

<p align="center">
<img src="https://imgur.com/8qH28ve.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Wazuh Manager on Mimikatz detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/G0nYNc3.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Wazuh Manager on SSH Brute-force detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/NIGTFg8.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>TheHive on Mimikatz detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/iJooRn1.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>TheHive on SSH Brute-force detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/iCGRxKZ.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle on Mimikatz detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/CXZXLjh.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle on SSH Brute-force detection and response</b>
<br/>

<p align="center">
<img src="https://imgur.com/q4hQxPD.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Mimikatz attack notifcation is sent to analyst thru email</b>
<br/>

<p align="center">
<img src="https://imgur.com/RcaEoAU.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>SSH Brute-force attack notifcation is sent to analyst thru email</b>
<br/>

<p align="center">
<img src="https://imgur.com/aMAD2tQ.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Linux host. Attacker's IP address was blocked</b>
<br/>

<p align="center">
<img src="https://imgur.com/xlk4ipx.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Attacker's machine. Connections are blocked</b>
<br/>

## Outcome

- Comprehensive SOC Automation Setup
  - Successful creation and integration of a SOC automation environment, including Wazuh for monitoring, automated workflows in Shuffle for alert management and incident response, and TheHive for case management.
 
- Practical Cybersecurity Skills
  - Hands-on experience in installing, configuring, and integrating various cybersecurity tools, enhancing proficiency in SOC operations.

- Effective Threat Detection and Response
  - Ability to configure and utilize telemetry for monitoring, detect specific threats through custom alerts, and automate incident response actions.

- Enhanced Cybersecurity Capabilities
  - Proficiency in creating efficient workflows and automated responses, improving overall security posture and operational efficiency.

- Encountered
  - AWS EC2 Instance. There were cases where a shutdown was necessary, and the public IP address changed each time the system was restarted after a shutdown.

## Acknowledgements
- [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- Sysmon config inspired from [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
- SOC Automation Project Lab inspired from [MyDFIR](https://github.com/MyDFIR/SOC-Automation-Project)
- Mimikatz from [Benjamin DELPY](https://github.com/gentilkiwi/mimikatz)
- Hydra from [Van Hauser-THC](https://github.com/vanhauser-thc/thc-hydra)
