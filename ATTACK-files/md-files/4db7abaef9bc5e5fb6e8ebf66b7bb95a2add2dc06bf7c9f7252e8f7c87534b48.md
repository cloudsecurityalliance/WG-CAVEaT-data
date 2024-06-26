3/22/24, 3:37 PM Account Manipulation: Additional Container Cluster Roles, Sub-technique T1098.006 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1098/006/ 1/4Thank you to Tidal Cyber and SOC Prime for becoming ATT&CK's ﬁrst Benefactors. To join the cohort, or learn more about this program visit our
Benefactors page.3/22/24, 3:37 PM Account Manipulation: Additional Container Cluster Roles, Sub-technique T1098.006 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1098/006/ 2/4Home>Techniques>Enterprise>Account Manipulation>Additional Container Cluster Roles3/22/24, 3:37 PM Account Manipulation: Additional Container Cluster Roles, Sub-technique T1098.006 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1098/006/ 3/4Account Manipulation: Additional Container Cluster
Roles
Mitigations
ID Mitigation Description
M1032 Multi-factor
AuthenticationRequire multi-factor authentication for user accounts integrated into container clusters through cloud
deployments or via authentication protocols such as LDAP or SAML.
M1018 User Account
ManagementEnsure that low-privileged accounts do not have permissions to add permissions to accounts or to
update container cluster roles.
Detection
ID Data Source Data Component Detects
DS0002 User AccountUser Account
ModiﬁcationCollect usage logs from accounts to identify unusual activity in the assignment of roles
to those accounts. Monitor for accounts assigned to high-privileged cluster roles that go
over a certain threshold of known admins.An adversary may add additional roles or permissions to an adversary-controlled user or service account to maintain persistent access to a
container orchestration system. For example, an adversary with suﬃcient permissions may create a RoleBinding or a ClusterRoleBinding to
bind a Role or ClusterRole to a Kubernetes account. Where attribute-based access control (ABAC) is in use, an adversary with suﬃcient
permissions may modify a Kubernetes ABAC policy to give the target account additional permissions.
This account modiﬁcation may immediately follow Create Account or other malicious account activity. Adversaries may also modify existing
Valid Accounts that they have compromised.
Note that where container orchestration systems are deployed in cloud environments, as with Google Kubernetes Engine, Amazon Elastic
Kubernetes Service, and Azure Kubernetes Service, cloud-based role-based access control (RBAC) assignments or ABAC policies can often be
used in place of or in addition to local permission assignments. In these cases, this technique may be used in conjunction with
Additional Cloud Roles.Other sub-techniques of Account Manipulation (6)
[1][2]
[3]
[4][5][6]
Version PermalinkID: T1098.006
Sub-technique of:  T1098

Tactics: Persistence, Privilege Escalation

Platforms: Containers
Version: 1.0
Created: 14 July 2023
Last Modiﬁed: 16 October 20233/22/24, 3:37 PM Account Manipulation: Additional Container Cluster Roles, Sub-technique T1098.006 - Enterprise | MITRE ATT&CK®
https://attack.mitre.org/techniques/T1098/006/ 4/4References
1. Kubernetes. (n.d.). Role Based Access Control Good Practices.
Retrieved March 8, 2023.
2. Michael Katchinskiy, Assaf Morag. (2023, April 21). First-Ever
Attack Leveraging Kubernetes RBAC to Backdoor Clusters.
Retrieved July 14, 2023.
3. Kuberenets. (n.d.). Using ABAC Authorization. Retrieved July
14, 2023.4. Google Cloud. (n.d.). Create IAM policies. Retrieved July 14,
2023.
5. Amazon Web Services. (n.d.). IAM roles for service accounts.
Retrieved July 14, 2023.
. Microsoft Azure. (2023, April 28). Access and identity options
for Azure Kubernetes Service (AKS). Retrieved July 14, 2023.