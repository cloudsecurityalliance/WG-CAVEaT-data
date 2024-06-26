3/24/24, 10:45 AM External Remote Services, Technique T0822 - ICS | MITRE ATT&CK®
https://attack.mitre.org/techniques/T0822/ 1/4Thank you to Tidal Cyber and SOC Prime for becoming ATT&CK's ﬁrst Benefactors. To join the cohort, or learn more about this program visit our
Benefactors page.3/24/24, 10:45 AM External Remote Services, Technique T0822 - ICS | MITRE ATT&CK®
https://attack.mitre.org/techniques/T0822/ 2/4Home>Techniques>ICS>External Remote Services3/24/24, 10:45 AM External Remote Services, Technique T0822 - ICS | MITRE ATT&CK®
https://attack.mitre.org/techniques/T0822/ 3/4External Remote Services
Procedure Examples
ID Name Description
C0028 2015 Ukraine Electric
Power AttackDuring the 2015 Ukraine Electric Power Attack, Sandworm Team used Valid Accounts taken from the
Windows Domain Controller to access the control system Virtual Private Network (VPN) used by grid
operators. 
C0020 Maroochy Water
BreachIn the Maroochy Water Breach, the adversary gained remote computer access to the system over
radio.
Targeted Assets
ID Asset
A0008 Application Server
A0009 Data Gateway
A0006 Data Historian
A0012 Jump Host
A0014 Routers
A0011 Virtual Private Network (VPN) ServerAdversaries may leverage external remote services as a point of initial access into your network. These services allow users to connect to
internal network resources from external locations. Examples are VPNs, Citrix, and other access mechanisms. Remote service gateways
often manage connections and credential authentication for these services. 
External remote services allow administration of a control system from outside the system. Often, vendors and internal engineering groups
have access to external remote services to control system networks via the corporate network. In some cases, this access is enabled directly
from the internet. While remote access enables ease of maintenance when a control system is in a remote area, compromise of remote
access solutions is a liability. The adversary may use these services to gain access to and execute attacks against a control system network.
Access to valid accounts is often a requirement.
As they look for an entry point into the control system network, adversaries may begin searching for existing point-to-point VPN
implementations at trusted third party networks or through remote support employee connections where split tunneling is enabled. [1]
[2]
Version PermalinkID: T0822
Sub-techniques:  No sub-techniques
 
Tactic: Initial Access
 
Platforms: None
Version: 1.1
Created: 21 May 2020
Last Modiﬁed: 13 October 2023
[3]
[4]3/24/24, 10:45 AM External Remote Services, Technique T0822 - ICS | MITRE ATT&CK®
https://attack.mitre.org/techniques/T0822/ 4/4Mitigations
ID Mitigation Description
M0936 Account Use Policies Conﬁgure features related to account use like login attempt lockouts, speciﬁc login times, and
password strength requirements as examples. Consider these features as they relate to assets which
may impact safety and availability. 
M0942 Disable or Remove
Feature or ProgramConsider removal of remote services which are not regularly in use, or only enabling them when
required (e.g., vendor remote access). Ensure all external remote access point (e.g., jump boxes, VPN
concentrator) are conﬁgured with least functionality, especially the removal of unnecessary services.
M0935 Limit Access to
Resource Over
NetworkLimit access to remote services through centrally managed concentrators such as VPNs and other
managed remote access systems.
M0932 Multi-factor
AuthenticationUse strong multi-factor authentication for remote service accounts to mitigate an adversary's ability
to leverage stolen credentials. Be aware of multi-factor authentication interception techniques for
some implementations.
M0930 Network
SegmentationDeny direct remote access to internal systems through the use of network proxies, gateways, and
ﬁrewalls. Consider a jump server or host into the DMZ for greater access control. Leverage this DMZ
or corporate resources for vendor access. 
M0927 Password Policies Set and enforce secure password policies for accounts.
M0918 User Account
ManagementConsider utilizing jump boxes for external remote access. Additionally, dynamic account
management may be used to easily remove accounts when not in use.
Detection
ID Data Source Data Component Detects
DS0015 Application Log Application Log
ContentWhen authentication is not required to access an exposed remote service, monitor for
follow-on activities such as anomalous external use of the exposed API or
application.
DS0028 Logon Session Logon Session
MetadataMonitor authentication logs and analyze for unusual access patterns, windows of
activity, and access outside of normal business hours, including use of Valid
Accounts.
DS0029 Network Traﬃc Network Traﬃc
FlowMonitor for network traﬃc originating from unknown/unexpected systems.
References[5]
[6]
[5]
1. Daniel Oakley, Travis Smith, Tripwire Retrieved. 2018/05/30
2. Electricity Information Sharing and Analysis Center; SANS
Industrial Control Systems 2016, March 18 Analysis of the
Cyber Attack on the Ukranian Power Grid: Defense Use Case
Retrieved. 2018/03/27
3. Booz Allen Hamilton When The Lights Went Out Retrieved.
2019/10/224. Marshall Abrams 2008, July 23 Malicious Control System
Cyber Security Attack Case Study Maroochy Water Services,
Australia Retrieved. 2018/03/27
5. Keith Stouffer 2015, May Guide to Industrial Control Systems
(ICS) Security Retrieved. 2018/03/28
 . Department of Homeland Security 2016, September Retrieved.
2020/09/25