# Welcome!!!

## $nslookup
<a href="https://www.linkedin.com/in/edisonward/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

## $whoami
I'm Edison Ward. Aspiring Cybersecurity Analyst with a track record of over six years in diagnosing and rectifying diverse computer and network-related challenges. A distinguished Navy veteran, offering a decade-long history of fostering teamwork, accountability, and strong work ethics. Results-orientated with a commitment to continual learning and interpersonal adeptness. Highly driven and meticulously poised to contribute to organizational objectives.

## $history
Executive IT Support Specialist
<br> Bill & Melinda Gates Foundation, Nov 2021 - Mar 2024

-	Delivered 24/7 high-touch technical support tailored for executives, directors, and VIPs.
-	Ensured adherence to security policies by leveraging endpoint management solutions, Microsoft Intune and Workspace ONE, effectively bringing numerous devices into compliance and safeguarding access to system resources.
-	Managed the domain accounts of over 1,500 users, utilizing IAM solutions, Active Directory and Azure AD, assuring the right users have the appropriate access to technology resources.

Technical Support Specialist
<br> Intellectual Ventures, Feb 2019 - Mar 2021

-	Addressed a broad spectrum of technical challenges spanning multiple platforms and applications, catering to clientele across diverse time zones.
-	Leveraged phishing analysis tools like URL2PNG, VirusTotal, and Whois, to proactively thwart phishing attacks, thereby mitigating risks associated with credential theft and malware infiltration.
-	Enhanced system security and performance by meticulously executing monthly server patches through SCCM and OS updates.

Amazon Live Stream Event Associate
<br> Amazon, Jan 2019 - Feb 2019

-	Successfully managed multiple concurrent live streaming events, assuming full ownership of numerous tier 1 live events to ensure unparalleled customer experience and satisfaction.
-	Bolstered operational enhancements by driving process improvements and implementing automation initiatives to streamline workflows and optimize efficiency.
-	Collaborated closely with senior engineers and cross-functional teams to effectively transition active support issues, prioritizing root-cause analysis and fostering the creation of a comprehensive team-specific knowledge base and skill set.

Network Operations Center Analyst
<br> Wave Broadband, Oct 2015 - Jun 2017

-	Monitored and triaged the Wave network and its subsidiaries across multiple states, utilizing network monitoring solutions such as OpenNMS and SolarWinds to uphold service level agreements and operational efficiency.
-	Troubleshot network issues through CLI and GUI across various router and switch models, including Cisco, Juniper, Arris, and ADVA, minimizing downtime and network congestion.
-	Provided tiered escalation support for Technical Support Representatives and extended installation and troubleshooting assistance for Field Technicians, ensuring prompt resolution of technical issues and uninterrupted service delivery.

Aviation Electronics Technician (Former TS/SCI and Secret Clearance)
<br> US Navy, Jul 2004 - Sep 2013

- Proficiently maintained and serviced critical avionic systems onboard mission aircraft, ensuring optimal performance and reliability in high-stakes operational environments.
- Provided comprehensive training and qualification to numerous personnel in military-related disciplines, contributing to the readiness and proficiency of the workforce.
- Directed and supervised daily operations within the work center, ensuring the timely completion of priorities set forth by management and maintaining operational continuity.

## $ls education and certifications
Education:
- Bachelor of Science in Cybersecurity and Information Assurance
<br>City University of Seattle | Seattle, WA
<br>Jun 2019

- Associate of Applied Science in Network Systems Administration
<br>ITT Technical Institute | Seattle, WA
<br>Sep 2016

Certifications:
- <a href="https://www.credly.com/badges/f61f9bc7-b044-4be5-ab73-b5c304597854/public_url">CompTIA A+</a>
- Cybrary SOC Analyst
- <a href="https://www.credly.com/badges/cff68502-f364-493f-b028-9cc492076d05/public_url">CompTIA Security+</a>
- Consortium for Service Innovation - KCS v6 Fundamentals
- <a href="https://www.coursera.org/account/accomplishments/verify/53XN438CZMC5">Google - Technical Support Fundamentals</a>
- <a href="https://www.coursera.org/account/accomplishments/verify/RH4P8BV7F2WX">Palo Alto Networks Cybersecurity Foundation</a>
- Qualys Certified Specialist
- <a href="https://www.credly.com/badges/f85d4be6-6aff-4abc-abf5-294f9105fa9a/public_url">Security Blue Team - Blue Team Level 1</a>
- <a href="https://www.credly.com/badges/30787a57-9ccc-4255-a608-e6f2fd96cd71/public_url">Splunk Core Certified User</a>

## $cat projects & skills
Projects:
- Personal Projects:
  - C2 Framework Emulating Threat Actor Behavior, and Detection and Response Through EDR (file attachment coming soon)
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
    - Added YARA rules in LimaCharlie to detect Sliver implants in Windows and Linux. Also, added generic detection and response rules to generate alerts whenever a YARA detection occurs.
    - Since the C2 payload is still in the host machine, a YARA scan was performed on the host machine to ensure that the YARA rules worked using LimaCharlie. It worked as the C2 payload was detected.
    - Created a rule in LimaCharlie to detect any new .exe files appearing in any user's Downloads directory of the host machine, report it, and kick off a YARA scan of the file path.
    - Created a rule in LimaCharlie to detect any process launched from any user's Downloads directory of the host machine, report it, and kick off a YARA scan of the process ID.
    - Moved the C2 payload from the Downloads to the Documents directory on the host machine. Placed the C2 payload back in the Downloads directory. LimaCharlie detected the C2 payload being dropped in the Downloads directory and kicked off a YARA scan that found the C2 payload inside.
    - Executed the C2 payload from the host machine. LimaCharlie detected the execution and kicked off a YARA scan that found the C2 payload in the Downloads directory.

- Learning Platforms:
  - <a href="https://app.cybrary.it/profile/EdisonWard">Cybrary</a>
  - <a href="https://blueteamlabs.online/public/user/4e09fa1f9ff9d63f0abcde">Blue Team Labs Online:
    - <a href="https://blueteamlabs.online/achievement/share/75272/203">Reverse Engineering</a>
      - Used Detect it Easy to gather information about a file such as its hash, the language it was written in, the section of the file that is highly entropic-packed (compressed) usually considered malicious, and its C2 domain.
      - Employed SigCheck to verify if a file has been signed with a code-signing certificate proving its validity.
      - Enabled Windows Defender and verified malware by scanning a suspected file.
      - Utilized Timeline Explorer to organize and search through threat logs.
      - Applied the MITRE ATT&CK framework to analyze the techniques and tactics used. 

Skills:
- Customer Service
- Digital Forensics - Autopsy, Volatility, Process Explorer
- Email Gateway - Microsoft Exchange and Microsoft Exchange Online
- Endpoint Management - Microsoft Intune, SCCM, Workspace ONE
- Endpoint Security - EDR (LimaCharlie, Wazuh), Microsoft Defender Antivirus
- IAM - Active Directory, Azure Active Directory
- Incident Response - Wireshark, DeepBlueCLI
- Knowledge Management - SharePoint, Zendesk, Confluence
- Log Analysis - SIEM (Splunk, Wazuh), Windows Event Logs, Sysmon
- Network Monitoring - OpenNMS, SolarWinds
- Network Security - IDS/IPS (Snort), Firewall (Windows Defender Firewall, iptables), VPN (Global Protect, DirectAccess, Appgate SDP)
- Networking - Cisco, ADVA, Arris, Juniper
- Operating Systems: Windows, Linux, MacOS, iOS, Android
- Penetration Testing - Nmap/Zenmap, John the Ripper
- Phishing Analysis - URL2PNG, VirusTotal, Whois, Wannabrowser
- Printing - Xerox Workplace Cloud, Xerox Follow-You Printing
- Productivity Software - Office 365
- Project Management Software - Jira
- Remote Support - Tanium, BeyondTrust, LogMeIn Rescue
- Reverse Engineering - Detect it Easy, SigCheck, Timeline Explorer
- Scripting - PowerShell, Python
- Ticketing Systems - theHive, ServiceNow, Zendesk
- Threat Intelligence - MISP
- Video Conferencing Platforms- Microsoft Teams, Zoom
- Vulnerability Management - Qualys
