3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 1/8Thank you to Tidal Cyber and SOC Prime for becoming ATT&CK's ﬁrst Benefactors. To join the cohort, or learn more about this program visit our
Benefactors page.3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 2/8Home>Techniques>Enterprise>Fallback Channels3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 3/8Fallback Channels
Adversaries may use fallback or alternate communication channels if the primary channel is compromised or inaccessible in order to
maintain reliable command and control and to avoid data transfer thresholds.
Version PermalinkID: T1008
Sub-techniques:  No sub-techniques

Tactic: Command and Control

Platforms: Linux, Windows, macOS
Version: 1.0
Created: 31 May 2017
Last Modiﬁed: 14 July 20203/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 4/8Procedure Examples
ID Name Description
S0504 Anchor Anchor can use secondary C2 servers for communication after establishing connectivity and relaying
victim information to primary C2 servers.
S0622 AppleSeed AppleSeed can use a second channel for C2 when the primary channel is in upload mode.
G0096 APT41 APT41 used the Steam community page as a fallback mechanism for C2.
S0534 Bazar Bazar has the ability to use an alternative C2 server if the primary server fails.
S0017 BISCUIT BISCUIT malware contains a secondary fallback command and control server that is contacted after the
primary command and control server.
S0089 BlackEnergy BlackEnergy has the capability to communicate over a backup channel via plus.google.com.
S1039 Bumblebee Bumblebee can use backup C2 servers if the primary server fails.
S0348 Cardinal RAT Cardinal RAT can communicate over multiple C2 host and port combinations.
S0674 CharmPower CharmPower can change its C2 channel once every 360 loops by retrieving a new domain from the
actors’ S3 bucket.
S0023 CHOPSTICK CHOPSTICK can switch to a new C2 channel if the current one is broken.
S0538 Crutch Crutch has used a hardcoded GitHub repository as a fallback channel.
S0021 Derusbi Derusbi uses a backup communication method with an HTTP beacon.
S0062 DustySky DustySky has two hard-coded domains for C2 servers; if the ﬁrst does not respond, it will try the second.
S0377 Ebury Ebury has implemented a fallback mechanism to begin using a DGA when the attacker hasn't connected
to the infected system for three days.
S0401 Exaramel for
LinuxExaramel for Linux can attempt to ﬁnd a new C2 server if it receives an error.
S0512 FatDuke FatDuke has used several C2 servers per targeted organization.
G0046 FIN7 FIN7's Harpy backdoor malware can use DNS as a backup channel for C2 if HTTP fails.
S0666 Gelsemium Gelsemium can use multiple domains and protocols in C2.
S0376 HOPLIGHT HOPLIGHT has multiple C2 channels in place in case one fails.
S0260 InvisiMole InvisiMole has been conﬁgured with several servers available for alternate C2 communications.
S0044 JHUHUGIT JHUHUGIT tests if it can reach its C2 server by ﬁrst attempting a direct connection, and if it fails,
obtaining proxy settings and sending the connection through a proxy, and ﬁnally injecting code into a
running browser if the proxy method fails.
S0265 Kazuar Kazuar can accept multiple URLs for C2 servers.
S1020 Kevin Kevin can assign hard-coded fallback domains for C2.
S0236 Kwampirs Kwampirs uses a large list of C2 servers that it cycles through until a successful connection is
established.[1]
[2]
[3]
[4]
[5][6]
[7]
[8]
[9]
[10]
[11]
[12]
[13]
[14]
[15]
[16]
[17]
[18]
[19]
[20]
[21][22]
[23]
[24]
[25]
[26]3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 5/8ID Name Description
G0032 Lazarus Group Lazarus Group malware SierraAlfa sends data to one of the hard-coded C2 servers chosen at random,
and if the transmission fails, chooses a new C2 server to attempt the transmission again.
S0211 Linfo Linfo creates a backdoor through which remote attackers can change C2 servers.
S0409 Machete Machete has sent data over HTTP if FTP failed, and has also used a fallback server.
S0051 MiniDuke MiniDuke uses Google Search to identify C2 servers if its primary C2 method via Twitter is not working.
S0084 Mis-Type Mis-Type ﬁrst attempts to use a Base64-encoded network protocol over a raw TCP socket for C2, and if
that method fails, falls back to a secondary HTTP-based protocol to communicate to an alternate C2
server.
S0699 Mythic Mythic can use a list of C2 URLs as fallback mechanisms in case one IP or domain gets blocked.
S0034 NETEAGLE NETEAGLE will attempt to detect if the infected host is conﬁgured to a proxy. If so, NETEAGLE will send
beacons via an HTTP POST request; otherwise it will send beacons via UDP/6000.
C0002 Night Dragon During Night Dragon, threat actors used company extranet servers as secondary C2 servers.
G0049 OilRig OilRig malware ISMAgent falls back to its DNS tunneling mechanism if it is unable to reach the C2 server
over HTTP.
S0501 PipeMon PipeMon can switch to an alternate C2 domain when a particular date has been reached.
S0269 QUADAGENT QUADAGENT uses multiple protocols (HTTPS, HTTP, DNS) for its C2 server as fallback channels if
communication with one is unsuccessful.
S1084 QUIETEXIT QUIETEXIT can attempt to connect to a second hard-coded C2 if the ﬁrst hard-coded C2 address fails.
S0629 RainyDay RainyDay has the ability to switch between TCP and HTTP for C2 if one method is not working.
S0495 RDAT RDAT has used HTTP if DNS C2 communications were not functioning.
S0085 S-Type S-Type primarily uses port 80 for C2, but falls back to ports 443 or 8080 if initial communication fails.
S1019 Shark Shark can update its conﬁguration to use a different C2 server.
S0444 ShimRat ShimRat has used a secondary C2 location if the ﬁrst was unavailable.
S0610 SideTwist SideTwist has primarily used port 443 for C2 but can use port 80 as a fallback.
S0058 SslMM SslMM has a hard-coded primary and backup C2 string.
S0603 Stuxnet Stuxnet has the ability to generate new C2 domains.
S0586 TAINTEDSCRIBE TAINTEDSCRIBE can randomly pick one of ﬁve hard-coded IP addresses for C2 communication; if one of
the IP fails, it will wait 60 seconds and then try another IP address.
S0668 TinyTurla TinyTurla can go through a list of C2 server IPs and will try to register with each until one responds.
S0266 TrickBot TrickBot can use secondary C2 servers for communication after establishing connectivity and relaying
victim information to primary C2 servers.
S0022 Uroburos Uroburos can use up to 10 channels to communicate between implants.
S0476 Valak Valak can communicate over multiple C2 hosts.[27][28]
[29]
[30]
[31]
[32]
[33]
[34]
[35]
[36]
[37]
[38]
[39]
[40]
[41]
[32]
[42]
[43]
[44]
[45]
[46]
[47]
[48]
[1]
[49]
[50]3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 6/8ID Name Description
S0059 WinMM WinMM is usually conﬁgured with primary and backup domains for C2 communications.
S0117 XTunnel The C2 server used by XTunnel provides a port number to the victim to use as a fallback in case the
connection closes on the currently used port.
Mitigations
ID Mitigation Description
M1031 Network
Intrusion
PreventionNetwork intrusion detection and prevention systems that use network signatures to identify traﬃc for
speciﬁc adversary malware can be used to mitigate activity at the network level. Signatures are often for
unique indicators within protocols and may be based on the speciﬁc protocol used by a particular adversary
or tool, and will likely be different across various malware families and versions. Adversaries will likely
change tool C2 signatures over time or construct protocols in such a way as to avoid detection by common
defensive tools. 
Detection
ID Data Source Data Component Detects
DS0029 Network TraﬃcNetwork
Connection
CreationMonitor for newly constructed network connections that may use fallback or alternate
communication channels if the primary channel is compromised or inaccessible in
order to maintain reliable command and control and to avoid data transfer thresholds.
Processes utilizing the network that do not normally have network communication or
have never been seen before may be suspicious.
Note: Network Analysis frameworks such as Zeek can be used to capture, decode, and
alert on TCP network connection creation. The below analytic is using an event ID from
OSQuery.
Analytic 1 - Windows Process Network Connection
netcon\_from\_sysproc = filter process\_open\_sockets where remote\_port != 0
AND proc\_name!= '';"
Network Traﬃc
FlowMonitor network data for uncommon data ﬂows, such as unexpected surges or other
abnormal inbound/outbound patterns.[45]
[11]
[51]3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 7/8References
1. Dahan, A. et al. (2019, December 11). DROPPING ANCHOR:
FROM A TRICKBOT INFECTION TO THE DISCOVERY OF THE
ANCHOR MALWARE. Retrieved September 10, 2020.
2. Jazi, H. (2021, June 1). Kimsuky APT continues to target
South Korean government using AppleSeed backdoor.
Retrieved June 10, 2021.
3. Fraser, N., et al. (2019, August 7). Double DragonAPT41, a
dual espionage and cyber crime operation APT41. Retrieved
September 23, 2019.
4. Pantazopoulos, N. (2020, June 2). In-depth analysis of the
new Team9 malware family. Retrieved December 1, 2020.
5. Mandiant. (n.d.). APT1 Exposing One of China’s Cyber
Espionage Units. Retrieved July 18, 2016.
. Mandiant. (n.d.). Appendix C (Digital) - The Malware Arsenal.
Retrieved July 18, 2016.
7. Baumgartner, K. and Garnaeva, M.. (2014, November 3). BE2
custom plugins, router abuse, and target proﬁles. Retrieved
March 24, 2016.
. Merriman, K. and Trouerbach, P. (2022, April 28). This isn't
Optimus Prime's Bumblebee but it's Still Transforming.
Retrieved August 22, 2022.
9. Grunzweig, J.. (2017, April 20). Cardinal RAT Active for Over
Two Years. Retrieved December 8, 2018.
10. Check Point. (2022, January 11). APT35 exploits Log4j
vulnerability to distribute new modular PowerShell toolkit.
Retrieved January 24, 2022.
11. ESET. (2016, October). En Route with Sednit - Part 2:
Observing the Comings and Goings. Retrieved November 21,
2016.
12. Faou, M. (2020, December 2). Turla Crutch: Keeping the “back
door” open. Retrieved December 4, 2020.
13. Fidelis Cybersecurity. (2016, February 29). The Turbo
Campaign, Featuring Derusbi for 64-bit Linux. Retrieved March
2, 2016.
14. ClearSky. (2016, January 7). Operation DustySky. Retrieved
January 8, 2016.
15. Vachon, F. (2017, October 30). Windigo Still not Windigone: An
Ebury Update . Retrieved February 10, 2021.
1. ANSSI. (2021, January 27). SANDWORM INTRUSION SET
CAMPAIGN TARGETING CENTREON SYSTEMS. Retrieved
March 30, 2021.
17. Faou, M., Tartare, M., Dupuy, T. (2019, October). OPERATION
GHOST. Retrieved September 23, 2020.
1. Crowdstrike. (2020, March 2). 2020 Global Threat Report.
Retrieved December 11, 2020.
19. Dupuy, T. and Faou, M. (2021, June). Gelsemium. Retrieved
November 30, 2021.
20. US-CERT. (2019, April 10). MAR-10135536-8 – North Korean
Trojan: HOPLIGHT. Retrieved April 19, 2019.
21. Hromcová, Z. (2018, June 07). InvisiMole: Surprisingly
equipped spyware, undercover since 2013. Retrieved July 10,
2018.
22. Hromcova, Z. and Cherpanov, A. (2020, June). INVISIMOLE:
THE HIDDEN PART OF THE STORY. Retrieved July 16, 2020.
23. ESET. (2016, October). En Route with Sednit - Part 1:
Approaching the Target. Retrieved November 8, 2016.
24. Levene, B, et al. (2017, May 03). Kazuar: Multiplatform
Espionage Backdoor with API Access. Retrieved July 17, 2018.27. Novetta Threat Research Group. (2016, February 24).
Operation Blockbuster: Unraveling the Long Thread of the
Sony Attack. Retrieved February 25, 2016.
2. Novetta Threat Research Group. (2016, February 24).
Operation Blockbuster: Remote Administration Tools &
Content Staging Malware Report. Retrieved March 16, 2016.
29. Zhou, R. (2012, May 15). Backdoor.Linfo. Retrieved February
23, 2018.
30. ESET. (2019, July). MACHETE JUST GOT SHARPER
Venezuelan government institutions under attack. Retrieved
September 13, 2019.
31. Kaspersky Lab's Global Research & Analysis Team. (2013,
February 27). The MiniDuke Mystery: PDF 0-day Government
Spy Assembler 0x29A Micro Backdoor. Retrieved April 5, 2017.
32. Gross, J. (2016, February 23). Operation Dust Storm. Retrieved
December 22, 2021.
33. Thomas, C. (n.d.). Mythc Documentation. Retrieved March 25,
2022.
34. FireEye Labs. (2015, April). APT30 AND THE MECHANICS OF
A LONG-RUNNING CYBER ESPIONAGE OPERATION. Retrieved
May 1, 2015.
35. McAfee® Foundstone® Professional Services and McAfee
Labs™. (2011, February 10). Global Energy Cyberattacks:
“Night Dragon”. Retrieved February 19, 2018.
3. Falcone, R. and Lee, B. (2017, July 27). OilRig Uses ISMDoor
Variant; Possibly Linked to Greenbug Threat Group. Retrieved
January 8, 2018.
37. Tartare, M. et al. (2020, May 21). No “Game over” for the
Winnti Group. Retrieved August 24, 2020.
3. Lee, B., Falcone, R. (2018, July 25). OilRig Targets Technology
Service Provider and Government Agency with QUADAGENT.
Retrieved August 9, 2018.
39. Mandiant. (2022, May 2). UNC3524: Eye Spy on Your Email.
Retrieved August 17, 2023.
40. Vrabie, V. (2021, April 23). NAIKON – Traces from a Military
Cyber-Espionage Operation. Retrieved June 29, 2021.
41. Falcone, R. (2020, July 22). OilRig Targets Middle Eastern
Telecommunications Organization and Adds Novel C2
Channel with Steganography to Its Inventory. Retrieved July
28, 2020.
42. ClearSky Cyber Security . (2021, August). New Iranian
Espionage Campaign By “Siamesekitten” - Lyceum. Retrieved
June 6, 2022.
43. Yonathan Klijnsma. (2016, May 17). Mofang: A politically
motivated information stealing adversary. Retrieved May 12,
2020.
44. Check Point. (2021, April 8). Iran’s APT34 Returns with an
Updated Arsenal. Retrieved May 5, 2021.
45. Baumgartner, K., Golovkin, M.. (2015, May). The MsnMM
Campaigns: The Earliest Naikon APT Campaigns. Retrieved
April 10, 2019.
4. Nicolas Falliere, Liam O Murchu, Eric Chien 2011, February
W32.Stuxnet Dossier (Version 1.4) Retrieved. 2017/09/22
47. USG. (2020, May 12). MAR-10288834-2.v1 – North Korean
Trojan: TAINTEDSCRIBE. Retrieved March 5, 2021.
4. Cisco Talos. (2021, September 21). TinyTurla - Turla deploys
new malware to keep a secret backdoor on victim machines.
Retrieved December 2, 2021.
49. FBI et al. (2023, May 9). Hunting Russian Intelligence “Snake”
Malware. Retrieved June 8, 2023.3/22/24, 3:51 PM Fallback Channels, Technique T1008 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1008/ 8/825. Kayal, A. et al. (2021, October). LYCEUM REBORN:
COUNTERINTELLIGENCE IN THE MIDDLE EAST. Retrieved
June 14, 2022.
2. Symantec Security Response Attack Investigation Team.
(2018, April 23). New Orangeworm attack group targets the
healthcare sector in the U.S., Europe, and Asia. Retrieved May
8, 2018.50. Duncan, B. (2020, July 24). Evolution of Valak, from Its
Beginnings to Mass Distribution. Retrieved August 31, 2020.
51. Gardiner, J., Cova, M., Nagaraja, S. (2014, February).
Command & Control Understanding, Denying and Detecting.
Retrieved April 20, 2016.