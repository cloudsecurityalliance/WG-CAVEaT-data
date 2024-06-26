3/22/24, 3:34 PM Compromise Infrastructure, Technique T1584 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1584/ 1/4Thank you to Tidal Cyber and SOC Prime for becoming ATT&CK's ﬁrst Benefactors. To join the cohort, or learn more about this program visit our
Benefactors page.3/22/24, 3:34 PM Compromise Infrastructure, Technique T1584 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1584/ 2/4Home>Techniques>Enterprise>Compromise Infrastructure3/22/24, 3:34 PM Compromise Infrastructure, Technique T1584 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1584/ 3/4Compromise Infrastructure
Mitigations
ID Mitigation Description
M1056 Pre-
compromiseThis technique cannot be easily mitigated with preventive controls since it is based on behaviors performed
outside of the scope of enterprise defenses and controls.Adversaries may compromise third-party infrastructure that can be used during targeting. Infrastructure solutions include physical or cloud
servers, domains, and third-party web and DNS services. Instead of buying, leasing, or renting infrastructure an adversary may compromise
infrastructure and use it during other phases of the adversary lifecycle. Additionally, adversaries may compromise numerous
machines to form a botnet they can leverage.
Use of compromised infrastructure allows adversaries to stage, launch, and execute operations. Compromised infrastructure can help
adversary operations blend in with traﬃc that is seen as normal, such as contact with high reputation or trusted sites. For example,
adversaries may leverage compromised infrastructure (potentially also in conjunction with Digital Certiﬁcates) to further blend in and
support staged information gathering and/or Phishing campaigns. Additionally, adversaries may also compromise infrastructure to
support Proxy and/or proxyware services.
By using compromised infrastructure, adversaries may make it diﬃcult to tie their actions back to them. Prior to targeting, adversaries may
compromise the infrastructure of other adversaries.Sub-techniques (7)
[1][2][3][4]
[5]
[6][7]
[8]
Version PermalinkID: T1584
Sub-techniques:  T1584.001, T1584.002, T1584.003, T1584.004, T1584.005, T1584.006, T1584.007

Tactic: Resource Development

Platforms: PRE
Contributors: Goldstein Menachem; Jeremy Galloway; Shailesh Tiwary (Indian Army)
Version: 1.4
Created: 01 October 2020
Last Modiﬁed: 02 October 20233/22/24, 3:34 PM Compromise Infrastructure, Technique T1584 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1584/ 4/4Detection
ID Data Source Data Component Detects
DS0038 Domain NameActive DNS Monitor for queried domain name system (DNS) registry data that may compromise third-
party infrastructure that can be used during targeting. Detection efforts may be focused
on related stages of the adversary lifecycle, such as during Command and Control.
Domain
RegistrationConsider monitoring for anomalous changes to domain registrant information and/or
domain resolution information that may indicate the compromise of a domain. Efforts
may need to be tailored to speciﬁc domains of interest as benign registration and
resolution changes are a common occurrence on the internet.
Passive DNS Monitor for logged domain name system (DNS) data that may compromise third-party
infrastructure that can be used during targeting. Detection efforts may be focused on
related stages of the adversary lifecycle, such as during Command and Control.
DS0035 Internet Scan Response
ContentOnce adversaries have provisioned compromised infrastructure (ex: a server for use in
command and control), internet scans may help proactively discover compromised
infrastructure. Consider looking for identiﬁable patterns such as services listening,
certiﬁcates in use, SSL/TLS negotiation features, or other response artifacts associated
with adversary C2 software.
Response
MetadataMonitor for contextual data about an Internet-facing resource gathered from a scan, such
as running services or ports that may compromise third-party infrastructure that can be
used during targeting. Detection efforts may be focused on related stages of the
adversary lifecycle, such as during Command and Control.
References[9][10][11]
1. Mandiant. (n.d.). APT1 Exposing One of China’s Cyber
Espionage Units. Retrieved July 18, 2016.
2. ICANN Security and Stability Advisory Committee. (2005, July
12). Domain Name Hijacking: Incidents, Threats, Risks and
Remediation. Retrieved March 6, 2017.
3. Mercer, W., Rascagneres, P. (2018, November 27). DNSpionage
Campaign Targets Middle East. Retrieved October 9, 2020.
4. Winters, R. (2015, December 20). The EPS Awakens - Part 2.
Retrieved January 22, 2016.
5. Hirani, M., Jones, S., Read, B. (2019, January 10). Global DNS
Hijacking Campaign: DNS Record Manipulation at Scale.
Retrieved October 9, 2020.
. Amnesty International Security Lab. (2021, July 18). Forensic
Methodology Report: How to catch NSO Group’s Pegasus.
Retrieved February 22, 2022.7. Crystal Morin. (2023, April 4). Proxyjacking has Entered the
Chat. Retrieved July 6, 2023.
. NSA/NCSC. (2019, October 21). Cybersecurity Advisory: Turla
Group Exploits Iranian APT To Expand Coverage Of Victims.
Retrieved October 16, 2020.
9. ThreatConnect. (2020, December 15). Infrastructure Research
and Hunting: Boiling the Domain Ocean. Retrieved October 12,
2021.
10. Stephens, A. (2020, July 13). SCANdalous! (External Detection
Using Network Scan Data and Automation). Retrieved October
12, 2021.
11. Koczwara, M. (2021, September 7). Hunting Cobalt Strike C2
with Shodan. Retrieved October 12, 2021.