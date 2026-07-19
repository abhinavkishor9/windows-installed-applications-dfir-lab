# windows-installed-applications-dfir-lab
## Overview

This Digital Forensics and Incident Response (DFIR) lab demonstrates how investigators identify and analyze installed software on a Windows endpoint using native Windows utilities and Registry artifacts.

Installed applications often provide valuable evidence during malware investigations, insider threat cases, and endpoint compromise assessments. By correlating multiple Windows artifacts, investigators can determine whether software is legitimate, suspicious, or potentially related to malicious activity.

---

# Executive Summary

This investigation demonstrates how Windows stores information about installed applications across multiple system components. Using Windows Settings, Programs and Features, PowerShell, and Registry artifacts, installed software was enumerated and validated to build an inventory of applications present on the endpoint.

The investigation emphasizes evidence correlation and demonstrates how multiple sources can be used together to validate installed software without relying on third-party forensic tools.

---

# Learning Objectives

- Understand Windows software inventory artifacts.
- Investigate installed applications using multiple Windows utilities.
- Examine Registry uninstall keys.
- Correlate application information from different evidence sources.
- Identify potentially suspicious software.
- Document findings using a structured DFIR methodology.

---

# Skills Demonstrated

- Windows DFIR Investigation
- Software Inventory Analysis
- Registry Forensics
- Windows Registry Navigation
- PowerShell Enumeration
- Artifact Correlation
- Evidence Collection
- IOC Identification
- Software Validation
- Incident Documentation
- MITRE ATT&CK Mapping

---

# Tools Used

- Windows Settings
- Control Panel
- PowerShell
- Registry Editor (regedit)
- File Explorer

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 10 / Windows 11 |
| Investigation Type | Digital Forensics |
| Utilities | Native Windows Tools |
| Registry Artifact | HKLM\Software\Microsoft\Windows\CurrentVersion\Uninstall |
| Internet Required | No |

---

# Investigation Scenario

The SOC receives a report that unauthorized software may have been installed on a company workstation.

As the assigned DFIR analyst, your objective is to determine:

- Which applications are installed
- Who published the software
- Whether any applications appear suspicious
- Whether Registry artifacts support the software inventory

---

# Investigation Workflow

1. Create investigation workspace.
2. Review Installed Apps.
3. Examine Programs and Features.
4. Enumerate software using PowerShell.
5. Investigate Registry uninstall keys.
6. Correlate evidence.
7. Identify suspicious applications.
8. Document findings.

---

# MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Discovery | Software Discovery | T1518 |
| Discovery | System Information Discovery | T1082 |

### Why Software Discovery?

During post-compromise investigations, attackers frequently enumerate installed software to identify security products, administrative tools, virtualization software, or applications they can abuse. Likewise, investigators examine installed software to identify unauthorized applications or indicators of compromise.

---

# Evidence Collected

- Installed Apps inventory
- Programs and Features inventory
- PowerShell software enumeration
- Registry uninstall entries
- Application publisher information
- Software versions

---

# Evidence Correlation

| Evidence Source | Information Obtained | Investigation Value |
|-----------------|---------------------|--------------------|
| Windows Settings | Installed applications | Initial software inventory |
| Programs and Features | Installed date, publisher | Application validation |
| PowerShell | Registry enumeration | Independent verification |
| Registry Uninstall Keys | DisplayName, Publisher, Version | Primary forensic artifact |

Correlating multiple evidence sources improves confidence in forensic findings and reduces the likelihood of overlooking suspicious software.

---

# Investigation Findings

- Installed software inventory successfully collected.
- Registry artifacts accurately reflected installed applications.
- PowerShell enumeration matched Registry data.
- Application publishers were successfully validated.
- No unauthorized or suspicious software was identified during the investigation.

---

# Key Takeaways

- Installed software provides valuable forensic evidence during endpoint investigations.
- Registry uninstall keys are one of the primary artifacts used to enumerate installed applications.
- Multiple evidence sources should always be correlated before reaching investigative conclusions.
- Native Windows utilities provide sufficient visibility for basic software inventory investigations.

---

