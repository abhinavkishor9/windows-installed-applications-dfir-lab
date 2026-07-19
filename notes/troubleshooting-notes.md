# Troubleshooting Notes

## Issue 1 — Installed Application Missing

### Cause

Some portable applications are not registered with Windows.

### Resolution

Review application folders manually if required.

---

## Issue 2 — Programs Missing from Settings

### Cause

Some applications register only in Programs and Features or only in the Registry.

### Resolution

Always compare multiple evidence sources.

---

## Issue 3 — Registry Entry Not Found

### Cause

32-bit applications may be stored in:

HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall

### Resolution

Investigate both uninstall registry locations.

---

## Issue 4 — Publisher Unknown

### Cause

Poorly written software may not populate publisher information.

### Resolution

Verify executable properties and digital signatures if necessary.

---

## Issue 5 — PowerShell Returns Empty Fields

### Cause

Registry values may be incomplete.

### Resolution

Validate manually using Registry Editor.

---

# Lessons Learned

- Installed software should always be validated using multiple artifacts.
- Registry uninstall keys are primary forensic evidence.
- Unknown publishers require additional investigation.
- Evidence correlation improves confidence in forensic conclusions.
