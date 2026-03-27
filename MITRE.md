# MITRE ATT&CK Mapping

## ATT&CK Techniques Observed

| Tactic | Technique | ID | Evidence |
|--------|-----------|----|----------|
| Resource Development | Acquire Infrastructure: Domains | T1583.001 | The attacker used the typosquatted domain `letsdefwnd.io` to impersonate `letsdefend.io` |
| Initial Access | Phishing: Spearphishing Link | T1566.002 | The victim received an email containing a phishing link to `letsdefwnd.io` |
| Execution | User Execution: Malicious Link | T1204.001 | Endpoint telemetry confirmed the victim visited `https://letsdefwnd.io` |
| Command and Control / Network Communication | Application Layer Protocol: Web Protocols | T1071.001 | Network communication to `45.33.23.183` over HTTPS was observed |

---

## Why these mappings fit

### T1583.001 - Acquire Infrastructure: Domains
The suspicious domain `letsdefwnd.io` was clearly designed to imitate the legitimate `letsdefend.io` brand. This is consistent with attacker-owned domain infrastructure used to support phishing operations.

### T1566.002 - Phishing: Spearphishing Link
The phishing email delivered to `mateo@letsdefend.io` contained a social engineering lure and directed the recipient to a malicious link.

### T1204.001 - User Execution: Malicious Link
The endpoint evidence showed that the user clicked or otherwise accessed the malicious URL through Chrome.

### T1071.001 - Application Layer Protocol: Web Protocols
Proxy and endpoint telemetry confirmed HTTPS communication with the suspicious external infrastructure.

---

## Notes

This case does **not** include sufficient evidence to confidently map file execution, malware installation, persistence, credential dumping, or lateral movement. The observed evidence supports phishing delivery and user interaction, but not deeper compromise in the provided telemetry.
