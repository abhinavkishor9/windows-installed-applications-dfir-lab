# Investigation Notes

## Lab Summary

This investigation focused on identifying installed applications using native Windows forensic artifacts. Software inventory information was collected from Windows Settings, Control Panel, PowerShell, and Registry uninstall keys before correlating the evidence to validate application information.

---

## Analyst Methodology

The investigation followed a structured DFIR workflow:

1. Enumerate installed software using Windows Settings.
2. Validate applications through Programs and Features.
3. Query Registry uninstall keys using PowerShell.
4. Examine Registry artifacts manually using Registry Editor.
5. Correlate evidence across all sources.
6. Identify potentially suspicious applications.
7. Document investigative findings.

---

## Investigation Scenario

A workstation is suspected of containing unauthorized software.

The objective is to determine:

- Installed applications
- Software publishers
- Application versions
- Registry evidence
- Potentially suspicious software

---

## Evidence Collected

### Evidence 1 – Windows Settings

Collected:

- Application names
- Installed dates
- Publisher information

Finding:

Provided an initial software inventory.

---

### Evidence 2 – Programs and Features

Collected:

- Installed software
- Publisher
- Version

Finding:

Confirmed application inventory using a second evidence source.

---

### Evidence 3 – PowerShell Enumeration

Registry queried using PowerShell.

Collected:

- DisplayName
- Publisher
- DisplayVersion

Finding:

Registry enumeration matched installed software inventory.

---

### Evidence 4 – Registry Uninstall Keys

Registry Path

HKLM\Software\Microsoft\Windows\CurrentVersion\Uninstall

Collected:

- DisplayName
- Publisher
- Version
- Install information

Finding:

Registry artifacts confirmed installed applications.

---

## DFIR Analysis

Installed software information was successfully collected from multiple Windows artifacts.

Evidence correlation demonstrated consistency between:

- Windows Settings
- Programs and Features
- PowerShell
- Registry

No suspicious applications or unknown publishers were identified.

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Discovery | Software Discovery | T1518 |
| Discovery | System Information Discovery | T1082 |

---

## Analyst Observations

- Multiple Windows artifacts contained consistent software inventory information.
- Registry uninstall keys provided the most comprehensive application metadata.
- PowerShell enumeration simplified Registry analysis.
- Cross-validation increased confidence in investigative findings.
- No evidence of unauthorized software installation was identified.

---

## Conclusion

The investigation successfully demonstrated how installed software can be identified and validated using native Windows artifacts. By correlating Registry data with Windows software inventory utilities, investigators can efficiently identify legitimate and suspicious applications during endpoint investigations.
