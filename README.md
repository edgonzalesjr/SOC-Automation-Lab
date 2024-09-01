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
  - Automating alerts and notifications to analysts thru a Email/Discord channel
  - Utilizing VirusTotal for hash and IP address reputation checks
  - Configuring TheHive for case management

### Tools Used

- AWS EC2. Provides scalable computing capacity for applications and workloads. It is utilized for hosting servers.
- Wazuh. Offers security visibility into endpoints by monitoring their behavior and identifying threats, vulnerabilities, and anomalies.
- TheHive. A versatile security incident response tool, simplifies the creation, management, and analysis of security incidents.
- Shuffle. Automation for Security Orchestration Automation and Response.
- VirusTotal. Analyzes suspicious files, hash, IP address for malware and malicious content using antivirus engines and website scanners.
- Discord. Used to send notifications to analysts, prompting them to investigate incidents further.
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
  - Simulates as a on-prem server
  - Wazuh agent
  - SSH server installed (to simulate SSH bruteforce attack)

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
<img src="https://imgur.com/wlj9xEB.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>TheHive is running</b>
<br/>

<p align="center">
<img src="https://imgur.com/AIpiO93.png" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle for Windows 10 client</b>
<br/>

<p align="center">
<img src="https://imgur.com/VtjtNtx.png" height="40%" width="40%" alt="Device Specification"/>
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

- Server ingestion, analysis and alerts
<p align="center">
<img src="https://imgur.com/" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Wazuh Manager on Mimikatz detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Wazuh Manager on Mimikatz detection</b>
<br/>

<p align="center">
<img src="https://imgur.com/" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>TheHive on Mimikatz detection</b>
<br/>
  
<p align="center">
<img src="https://imgur.com/" height="40%" width="40%" alt="Device Specification"/>
<br/>
<b>Shuffle on Mimikatz detection</b>
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

## Acknowledgements
- [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- Sysmon config inspired from [Olaf Hartong](https://github.com/olafhartong/sysmon-modular)
- SOC Automation Project Lab inspired from [MyDFIR](https://github.com/MyDFIR/SOC-Automation-Project)
- Mimikatz from [Benjamin DELPY](https://github.com/gentilkiwi/mimikatz)
- Hydra from [Van Hauser-THC](https://github.com/vanhauser-thc/thc-hydra)
