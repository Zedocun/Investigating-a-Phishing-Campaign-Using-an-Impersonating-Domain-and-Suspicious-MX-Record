# Timeline

## Full Incident Timeline

| Date / Time | Source | Event |
|-------------|--------|-------|
| Sep 17, 2024 12:05 PM | Alert / Monitoring | Alert triggered: **SOC326 - Impersonating Domain MX Record Change Detected** |
| Sep 17, 2024 12:05 PM | Alert Details | Suspicious domain identified as `letsdefwnd.io` |
| Sep 17, 2024 12:05 PM | Alert Details | Suspicious MX record identified as `mail.mailerhost.net` |
| Sep 17, 2024 12:05 PM | Threat Intel | Domain `letsdefwnd.io` associated with phishing context |
| Sep 17, 2024 12:05 PM | Exchange Logs | Event observed from `no-reply@cti-report.io` to `soc@letsdefend.io` |
| Sep 17, 2024 12:05 PM | Exchange Logs | Source IP `64.233.180.27` connected to internal mail infrastructure `172.16.20.3` over port `25` |
| Sep 18, 2024 08:00 AM | Email Security | Phishing email delivered from `voucher@letsdefwnd.io` to `mateo@letsdefend.io` |
| Sep 18, 2024 08:00 AM | Email Security | Subject: `Congratulations! You've Won a Voucher` |
| Sep 18, 2024 08:00 AM | Email Content | Email body included phishing lure and the URL `http://letsdefwnd.io/` |
| Sep 18, 2024 08:00 AM | Exchange Logs | Activity observed from `45.33.23.183` to `172.16.20.3` over port `25` |
| Sep 18, 2024 01:32 PM | Proxy Logs | Internal host `172.16.17.162` connected to `45.33.23.183` over port `443` |
| 2024-09-18 13:32:13 | Endpoint Security | User `Mateo` accessed `https://letsdefwnd.io` |
| 2024-09-18 13:32:13 | Endpoint Security | Process `chrome.exe` recorded as the browsing process |
| Post-investigation | Endpoint Security | Host placed into containment |

---

## Timeline Summary

The attack chain began with the identification of a suspicious impersonating domain and malicious MX record. The domain was later confirmed to be associated with a phishing-tagged URL. A phishing email was then delivered to the user `Mateo`, who subsequently accessed the malicious domain through Chrome. Infrastructure logs and endpoint telemetry confirmed the interaction, and the host was isolated as a containment step.
