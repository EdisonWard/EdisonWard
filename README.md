# Hello, I'm Edison Ward
<a href="https://www.linkedin.com/in/edisonward/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

## About Me

Aspiring Cybersecurity Professional boasting a track record of over six years in diagnosing and rectifying diverse computer and network-related challenges. A distinguished Navy veteran, offering a decade-long history of fostering teamwork, accountability, and strong work ethics. Demonstrated proficiency in swiftly analyzing and resolving intricate and time-sensitive issues, showcasing a results-oriented approach. Exhibits a fervent commitment to continual learning and interpersonal adeptness. Highly driven and meticulous team member poised to contribute to organizational objectives.

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
- Digital Forensics - Autopsy and Volatility
- Firewalls - Windows Defender Firewall and iptables
- IAM - AD & Azure AD
- Incident Response - Wireshark and DeepBlueCLI
- Network Scanner - Nmap/Zenmap
- Knowledge Management - SharePoint, Zendesk and Confluence
- Networking - Cisco, ADVA, Arris, and Juniper
- Password Attacks - John the Ripper
- Phishing Analysis - URL2PNG, VirusTotal, Whois, and Wannabrowser
- Project Management Software - TheHive5 and Jira
- Reverse Engineering - Detect it Easy, SigCheck, and Timeline Explorer
- Scripting - PowerShell
- SIEM - Splunk
- Threat Intelligence - MISP
- Vulnerability Management - Qualys

## Education

Bachelor of Science in Cybersecurity and Information Assurance
<br>City University of Seattle

Associate of Applied Science in Network Systems Administration
<br>ITT Technical Institute

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

<a href="https://blog.ecapuano.com/p/so-you-want-to-be-a-soc-analyst-intro?utm_source=direct&utm_campaign=post&utm_medium=web&triedRedirect=true">Created a virtual SOC environment, set up a C2 framework for emulating threat actor behavior, threw attacks, caught the detections, and responded by reporting or blocking the intrusions using LimaCharlie EDR.</a>

- Set up a Ubuntu server to serve as an attack box.
- Built a Windows 11 host machine, installed and configured Sysmon, and disabled Windows Defender through Windows Security, Group Policy Editor, and Registry Editor.
- Installed LimaCharlie (EDR) into the host machine and configured LimaCharlie to ship the Sysmon event logs alongside its own EDR telemetry.
- SSH'ed into the attack box and installed Sliver, a C2 framework, to emulate threat actor behavior.
- Generated a C2 payload, spun up a temporary web server, and downloaded the C2 payload from the attack box to the host machine via the web server.
- Started the HTTP listener of Sliver on the attack box, executed the C2 payload from the host machine, interacted with the new C2 session on the attack box, and observed the telemetry in LimaCharlie.
- Ran "procdump -n lsass.exe -s lsass.dmp" from the attack box. This action is used to steal credentials.
- Detected the attack in LimaCharlie and built a rule to report the intrusion.
- Ran "procdump -n lsass.exe -s lsass.dmp" again from the attack box, and LimaCharlie detected and reported it.
- Ran "shell" from the attack box and ran "vssadmin delete shadows /all" to delete Volume Shadow Copies. This action is typically used for ransomware as it deletes backup copies or snapshots of computer files and volumes. LimaCharlie's default Sigma rules detected this attack. Created a detection and response rule to report such events and respond by killing the parent process responsible with the deny_tree for the "vssadmin delete shadows /all" command.
- Ran "vssadmin delete shadows /all" again from the attack box and the prompt "Shell Existed" popped up. This shows that the rule created work as LimaCharlie successfully killed the parent process of shell.
- <a href="https://blog.ecapuano.com/p/so-you-want-to-be-a-soc-analyst-part-54f?triedRedirect=true">Viewed the video for tuning false positives in LimaCharlie.
- Added YARA rules in LimaCharlie to detect Sliver implants in Windows and Linux. Also, added generic detection and response rules to generate alerts whenever a YARA detection occurs.
- Since the C2 payload is still in the host machine, a YARA scan was performed on the host machine to ensure that the YARA rules worked using LimaCharlie. It worked as the C2 payload was detected.
- Created a rule in LimaCharlie to detect any new .exe files appearing in any user's Downloads directory of the host machine, report it, and kick off a YARA scan of the file path.
- Created a rule in LimaCharlie to detect any process launched from any user's Downloads directory of the host machine, report it, and kick off a YARA scan of the process ID.
- Moved the C2 payload from the Downloads to the Documents directory on the host machine. Placed the C2 payload back in the Downloads directory. LimaCharlie detected the C2 payload being dropped in the Downloads directory and kicked off a YARA scan that found the C2 payload inside.
- Executed the C2 payload from the host machine. LimaCharlie detected the execution and kicked off a YARA scan that found the C2 payload in the Downloads directory.

## Hands-on Labs

Blue Team Labs Online
<br><a href="https://blueteamlabs.online/achievement/share/75272/203">Anakus - Reverse Engineering</a>

- Used Detect it Easy to gather information about a file such as its hash, the language it was written in, the section of the file that is highly entropic-packed (compressed) usually considered malicious, and its C2 domain.
- Employed SigCheck to verify if a file has been signed with a code-signing certificate proving its validity.
- Enabled Windows Defender and verified malware by scanning a suspected file.
- Utilized Timeline Explorer to organize and search through threat logs.
- Applied the MITRE ATT&CK framework to analyze the techniques and tactics used. 
