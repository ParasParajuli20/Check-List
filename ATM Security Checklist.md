# 🏧 ATM Security Checklist

A comprehensive checklist covering physical, logical, and application security for ATM systems.

---

## 📌 Physical Security

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| Presence of physical guards                      | Ensure that physical guards are present at ATM locations.                |
| Review of CCTV cameras                           | Verify that CCTV cameras are functioning and cover all critical areas.   |
| Presence of vault locks and switches             | Check the integrity and functionality of vault locks and switches.       |
| Vault passcode brute force                       | Test the strength of vault passcodes against brute-force attacks.        |
| Lock picking of ATM locks                        | Test locks (cash vault, CPU, etc.) for vulnerabilities.                  |
| Presence of PIN shield                           | Ensure the PIN shield is intact and functioning properly.                |
| Physical security bypass                         | Test bypassing physical security measures (alarms, sensors, etc.).       |
| Wireless HID bypass                              | Test HID devices (keyboard/mouse) for unauthorized access risks.         |
| Access using master key                          | Verify proper controls over vault & CPU master keys.                     |

---

## 🔐 Logical Security

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| Network access review                            | Review access controls, ACLs, and firewall configurations.               |
| Hardening review of routers & switches           | Assess security of passwords, services, patches, etc.                    |
| ATM validation review                            | Ensure correct responses to invalid PINs, blocked cards, etc.            |
| Alternate boot of ATMs                           | Test alternate boot mechanisms (USB, CD, etc.).                          |
| Disable USB/Autorun                              | Prevent unauthorized software execution.                                 |
| Hard disk encryption                             | Check for data-at-rest protection.                                       |
| Internal ATM communication review                | Assess encryption/authentication of internal messages.                   |
| Application whitelisting                         | Ensure only authorized apps run on ATM.                                  |
| Anti-malware capabilities                        | Confirm anti-malware is up-to-date and active.                           |
| ATM surveillance (logs)                          | Ensure events/logs are generated and monitored.                          |
| Password policy                                  | Evaluate complexity, rotation, lockout.                                  |
| Host firewalls                                   | Verify firewall presence and rules.                                      |
| Vulnerable operating systems                     | Identify/remediate outdated or EOL OSes.                                 |
| ATM network scanning & pentesting                | Identify open ports and vulnerabilities.                                 |
| ATM network architecture review                  | Evaluate segmentation and secure communication.                          |
| Alternate boot data exfiltration                 | Test if booting from external device allows data theft.                  |
| Network sniffing                                 | Detect possibility of intercepting unencrypted data.                     |
| Default supervisor credentials                   | Test weak/default credentials.                                           |
| Remote access via HID                            | Check for unauthorized control via local/remote HID.                     |
| Clear text storage of sensitive data             | Verify sensitive info is not stored in plaintext.                        |
| Clear text transmission of sensitive data        | Ensure data is encrypted in transit.                                     |
| ATM card cloning                                 | Identify vulnerabilities to skimming/cloning.                            |
| Malware injection & reverse shell access         | Check if persistent malicious access is possible.                        |
| ATM network monitoring                           | Evaluate SIEM/logging for anomalies.                                     |
| Anti-malware review                              | Ensure solutions are updated, configured, and working.                   |
| Security solutions & integration review          | Assess IDS/IPS, whitelisting, firewall, and logging setup.              |

---

## ✅ Compliance

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| Regulatory/central bank compliance               | Ensure compliance with governing standards.                              |
| PCI-DSS/PCI-DA certification review              | Verify current and valid certifications.                                 |

---

## 💻 Application Security

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| ATM application testing                          | Check for OWASP/SANS vulnerabilities.                                    |
| ATM penetration testing                          | Conduct complete security gap assessment.                                |
| Framework-based assessment                       | Align with security standards (NIST, ISO, etc.).                         |
| ATM API security testing                         | Test API security (authentication, authorization, etc.).                 |

---

## 🔄 Process Review

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| Remitting/debiting foreign transactions          | Evaluate foreign transaction handling.                                   |
| Review of zero balance accounts                  | Monitor/manage zero-balance accounts.                                    |
| Payment message approval                         | Review approval process for ATM messages.                                |
| Fraud detection process                          | Evaluate rules and prevention strategies.                                |
| KYC & risk profiling review                      | Verify KYC integration into ATM operations.                              |
| Incident management process                      | Review incident logging, escalation, and resolution.                     |

---

## ⚙️ Operational Control

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| Geo-tagging of ATM transactions                  | Assess geo-location tagging for fraud/risk.                              |
| Dormant/zero-balance account review              | Ensure secure handling of dormant accounts.                              |
| Remittance approval process                      | Evaluate accuracy and security of remittance.                            |
| Fraud risk management rules                      | Review rule effectiveness and coverage.                                  |
| Backup review                                    | Confirm backup policies and testing.                                     |

---

## 🛠 Technical Review

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| OS configuration review                          | Review patching, hardening, and settings.                                |
| Network device configuration review              | Assess router/firewall/switch settings.                                  |
| USB boot checks                                  | Prevent unauthorized alternate booting.                                  |
| Data exfiltration checks                         | Assess remote access or file transfer risks.                             |
| Network port access                              | Verify unnecessary ports are restricted.                                 |
| ATM switch access                                | Ensure switch/router access is tightly controlled.                       |
| ATM network access                               | Confirm connection only to authorized endpoints.                         |

---

## 🧪 ATM Interface Testing

| Test Case/Checklist Item                         | Objective                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------|
| API security testing                             | Validate ATM API for secure communication.                              |
| Transport confidentiality                        | Encrypt session data in transit (SSL/TLS, IPsec).                        |
| Message confidentiality                          | Prevent message eavesdropping.                                           |
| Message integrity                                | Validate message checksums/signatures.                                  |
| Server authentication                            | Confirm server identity and trust.                                       |
| User authentication                              | Validate user/cardholder authentication.                                 |
| Authorization                                    | Enforce role/rule-based ATM function access.                             |
| Schema validation                                | Confirm data conforms to expected format.                                |
| Content validation                               | Prevent malicious/malformed input.                                       |
| Message throughput                               | Review ATM interface performance/reliability.                           |
| XML DoS protection                               | Mitigate XML-based DoS attacks.                                          |
| Business logic bypass: Withdrawal limits         | Prevent circumvention of withdrawal rules.                               |
| Business logic bypass: Negative balance          | Prevent overdrafts or unauthorized overdrawing.                          |

---

 ---

> ⚠️ **Disclaimer:** Use this checklist only on applications you have permission to test.


