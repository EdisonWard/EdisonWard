# Hello, I'm Edison Ward
<a href="https://www.linkedin.com/in/edisonward/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

## About Me
Aspiring Cybersecurity Professional with over 6 years of technical experience troubleshooting computer and network-related issues. Honorably discharged Navy veteran with a decade of background in teamwork, accountability, and work ethic. Results-driven with notable success in analyzing, diagnosing, and resolving complex and urgent problems. Passionate and personable with an eagerness to learn from others. Highly motivated and detail-oriented team player ready to help achieve company goals.

## Education

Bachelor of Science in Cybersecurity and Information Assurance
<br>City University of Seattle

Associate of Applied Science in Network Systems Administration
<br>ITT Technical Institute

## Experience

Executive IT Support Specialist
<br> Bill & Melinda Gates Foundation, Nov 2021 - Mar 2024

- Brought countless devices into compliance using endpoint management solutions mitigating the exploitation of vulnerabilities. 
-	Analyzed phishing attacks through phishing analysis tools preventing credential harvesting and installation of malware. 
-	Managed domain accounts of over 1,500 users through identity and access management solutions ensuring the right users have the appropriate access to technology resources. 
-	Performed incident response with guidance from the incident response team avoiding financial and reputational damage to the company. 

Technical Support Specialist
<br> Intellectual Ventures, Feb 2019 - Mar 2021

-	Performed monthly server patches through SCCM and OS updates enhancing security and performance. 
-	Tested, deployed, and maintained OneDrive in the environment safeguarding data to the cloud preventing loss of work in case of computer failure.
-	Executed fast quality work related to computer and network-related issues resulting in the resolution of over 2,250 tickets swiftly getting satisfied customers back to their activities. 

Amazon Live Stream Event Associate
<br> Amazon, Jan 2019 - Feb 2019

-	Executed multiple live streaming events concurrently; being the sole owner of many tier 1 live events ensuring the highest customer quality experience.
-	Enhanced operations driving improvements and automation.
-	Worked with senior engineers and other teams for handing off or taking over active support issues prioritizing root-cause fixes and creating a team-specific knowledge base and skill set.

Network Operations Center Analyst
<br> Wave Broadband, Oct 2015 - Jun 2017

-	Monitored and triaged the Wave network and its subsidiaries throughout multiple states using OpenNMS, SolarWinds, and other general network health statistics ensuring the company stays within its SLA.
-	Troubleshot network issues using CLI and GUI on different switch and router types including but not limited to Cisco, ADVA, Arris, and Juniper limiting downtime and congestion.
-	Provided escalation support for Technical Support Representatives as well as install and trouble calls for Field Technicians.

Aviation Electronics Technician
<br> US Navy, Jul 2004 - Sep 2013

- Maintained and repaired highly valued avionic systems on mission aircrafts.
- Fixed high-priced specialty electronics saving the Navy over $675,000 in funding.
- Trained and qualified countless personnel in military-related qualifications.
- Supervised work center resulting in the completion of daily priorities coming from management.
- Former TS/SCI and Secret clearance.


## Skills and Tools

- Antivirus - Microsoft Defender Antivirus
- Digital Forensics - Autopsy
- Endpoint Management - Intune, SCCM, and Workspace ONE
- EDR - LimaCharlie
- Forensics - Autopsy and Volatility
- IAM - AD & Azure AD
- Incident Response - Wireshark and DeepBlueCLI
- Information Gathering - Nmap/Zenmap
- Knowledge Management - SharePoint, Zendesk and Confluence
- Networking - Cisco, ADVA, Arris, and Juniper
- Password Attacks - John the Ripper
- Phishing Analysis - URL2PNG, VirusTotal, Whois, and Wannabrowser
- Reverse Engineering - Detect it Easy, SigCheck, and Timeline Explorer
- Scripting - PowerShell
- SIEM - Splunk
- Threat Intelligence - MISP
- Vulnerability Management - Qualys

## Certifications

- <a href="https://www.credly.com/badges/f61f9bc7-b044-4be5-ab73-b5c304597854/public_url">CompTIA A+</a>
- <a href="https://www.credly.com/badges/cff68502-f364-493f-b028-9cc492076d05/public_url">CompTIA Security+</a>
- Consortium for Service Innovation - KCS v6 Fundamentals
- <a href="https://www.coursera.org/account/accomplishments/verify/53XN438CZMC5">Google - Technical Support Fundamentals</a>
- <a href="https://www.coursera.org/account/accomplishments/verify/RH4P8BV7F2WX">Palo Alto Networks Cybersecurity Foundation</a>
- Qualys - Vulnerability Management, Detection and Response
- <a href="https://www.credly.com/badges/f85d4be6-6aff-4abc-abf5-294f9105fa9a/public_url">Security Blue Team - Blue Team Level 1</a>
- <a href="https://www.credly.com/badges/30787a57-9ccc-4255-a608-e6f2fd96cd71/public_url">Splunk Core Certified User</a>

## Projects

Endpoint Detection and Response Lab Using LimaCharlie

- Created up a small virtual environment

Built a virtual environment consisting of a Ubuntu server as a C2 attack box and a Windows 11 as the host machine. Configured the attack box with a static address and enabled secure remote access by installing OpenSSH. Installed Sliver on the attack system to provide advanced capabilities for covertly managing and controlling remote systems. Disabled Windows Defender through Windows Security, Group Policy Editor, and Registry Editor. Installed Sysmon on the host as it provides very granular telemetry from Windows endpoints. LimaCharlie is a very powerful “SecOps Cloud Platform”. It not only comes with a cross-platform EDR agent, but also handles all of the log shipping/ingestion and has a threat detection engine. Signed up for LimaCharlie's cloud service and installed one of its sensors on the host machine. Configured LimaCharlie to ship Sysmon event logs along with its own EDR telemetry.

- Executed a C2 payload and interacted with the host machine

Generated a C2 payload and spun up a temporary web server from the attack box. Downloaded the C2 payload from the attack box to the host machine. Started the Sliver HTTP listener on the attack box and executed the C2 payload from the host machine. Connected with the C2 session and is now interacting with the host machine. Observed the telemetry in LimaCharlie. Saw that the process for the C2 payload did not have a valid signature and was active on the network on the Processes tab. Was able to get the attack box IP address from the Network tab. Scanned the C2 payload using VirusTotal from the File System tab but the item was not found. The Timeline tab showed when the implant was created on the system, when it was launched shortly after, and the network connections it created immediately after.

- Emulated an adversary for crafting detections

Ran "procdump -n lsass.exe -s lsass.dmp" to dump the lsass.exe process from memory, stealing credentials. LimaCharlie detected this telemetry as "SENSITIVE_PROCESS_ACCESS" events in the Timeline tab. Used one of the events to build a detection and response rule to detect similar events going forward, respond to them by reporting them as "LSASS access" in the Detections tab, and tested the event to ensure that the detection would work before saving the rule. Reran the credential dumping command and LimaCharlie detected the attack in the Detections tab and showed it in the Timeline tab.

- Blocked an attack

Ran "shell" in the Sliver C2 shell then ran "vssadmin delete shadows /all" to erase backup copies or snapshots of computer files or volumes. This is often used for ransomware attacks. LimaCharlie's Detection tab was able to pick up this event through its default Sigma rules. Crafted a rule using the event to detect and report the event, and respond by killing the parent process responsible with "deny_tree" for the "vssadmin delete shadows /all" command. Ran "vssadmin delete shadows /all" from the attack box but the prompt "Shell Exited" came up effectively terminating the parent process.

- Triggered YARA scans with a detection rule

Created a YARA rule in LimaCharlie that detects Sliver Windows and Linux implants based on paths and function names within the binary. Created another YARA rule that detects Sliver Windows and Linux implants based on obvious strings within. Created a "D&R" rules in the Automation tab detecting and reporting YARA detections not involving a PROCESS object. Created another "D&R" rules in the Automation tab detecting and reporting YARA detections specifically involving a PROCESS object. Ran the following sensor command "yara_scan hive://yara/sliver -f C:\Users\User\Downloads\PROGRESSING_FRIENDLY.exe in the Console tab against the host machine. The output indicated a positive hit on one of the signatures contained within the Sliver YARA rule.The event was also detected on the Detections tab. Created a "D&R" rule in the automation tab to detect and report any new .exe files that appear in any user Downloads directory in the host machine. Created a "D&R" rule in the automation tab to detect and report any new .exe files that appear in any user Downloads directory in the host machine.
