# 🛰️ SolarWinds Supply Chain Breach Analysis

## 📌 Project Summary
In this independent project, I performed an in-depth analysis of the infamous SolarWinds supply chain breach. Rather than simulate the breach, the goal was to study it from a strategic cybersecurity perspective, understanding how the breach occurred, what the attackers did, and how a strong security posture could have prevented or mitigated the impact. This project showcases my ability to think critically as a security engineer and apply incident response and governance frameworks to a high-level attack.

## 🧠 What Happened During the Attack?
- **Year:** 2020
- **Target:** SolarWinds Orion Platform (used by U.S. government & Fortune 500s)
- **Initial Access:** Supply chain compromise
- **Malware:** SUNBURST backdoor injected in a software update
- **Impact:** Gave adversaries remote access to victims' networks for months
- **Threat Actor:** Allegedly APT29 (Russian SVR)

## 🛠️ TTPs Used by the Adversaries
| Tactic            | Technique                        | MITRE ID  |
| ----------------- | -------------------------------- | --------- |
| Initial Access    | Supply Chain Compromise          | T1195     |
| Command & Control | Application Layer Protocol       | T1071.001 |
| Defense Evasion   | Obfuscated Files or Information  | T1027     |
| Lateral Movement  | Remote Services (RDP, WMI, etc.) | T1021     |

## 📉 What Went Wrong?
- Lack of rigorous code validation before pushing updates
- Overprivileged Orion systems (easy lateral movement)
- Delayed detection — adversaries remained undetected for months
- Inadequate network segmentation

## 🛡️ How I Would Have Prevented / Detected This
- ✅ Isolate update systems in a zero-trust architecture
- ✅ Implement strict code-signing integrity validation
- ✅ Monitor outbound beaconing with a next-gen SIEM (like Splunk)
- ✅ Flag anomalous Orion behavior (e.g., registry tampering, external C2)
- ✅ Use behavior-based threat detection (MITRE ATT&CK-aligned)

## 📐 NIST Incident Response Framework Mapping
| Phase          | Response in Context                     |
| -------------- | --------------------------------------- |
| 1. Preparation | Threat modeling for supply chain risk   |
| 2. Detection   | Alert on unusual Orion behavior         |
| 3. Containment | Network segmentation & policy blocking  |
| 4. Eradication | Remove malicious Orion update & implant |
| 5. Recovery    | Restore from secure backups, full audit |

## 💬 Lessons Learned
This case highlights the importance of:
- Continuous supply chain risk assessment
- Investing in behavior-based detection
- Aligning IR processes with known frameworks

## 🔗 References
- [SolarWinds Attack Summary - CISA](https://www.cisa.gov/news-events/news/summary-solarwinds-supply-chain-attack)
- [MITRE ATT&CK Techniques](https://attack.mitre.org/)
