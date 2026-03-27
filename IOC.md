# Indicators of Compromise (IOCs)

## Domains

| IOC | Type | Context |
|-----|------|---------|
| `letsdefwnd.io` | Domain | Typosquatted phishing domain impersonating `letsdefend.io` |

---

## Email Addresses

| IOC | Type | Context |
|-----|------|---------|
| `voucher@letsdefwnd.io` | Email Address | Sender of phishing email to the victim |
| `no-reply@cti-report.io` | Email Address | Sender of security notification email to SOC |

---

## IP Addresses

| IOC | Type | Context |
|-----|------|---------|
| `45.33.23.183` | IP Address | Infrastructure associated with phishing email and web communication |
| `64.233.180.27` | IP Address | Observed in Exchange notification-related mail flow |
| `172.16.17.162` | Internal Host IP | Internal host involved in proxy/firewall traffic |
| `172.16.20.3` | Internal Mail IP | Internal mail infrastructure observed in Exchange logs |

---

## Infrastructure

| IOC | Type | Context |
|-----|------|---------|
| `mail.mailerhost.net` | MX Record | Suspicious MX record associated with `letsdefwnd.io` |
| `ns1.giantpanda.com` | Name Server | Name server associated with suspicious domain |
| `ns2.giantpanda.com` | Name Server | Name server associated with suspicious domain |

---

## URLs

| IOC | Type | Context |
|-----|------|---------|
| `http://letsdefwnd.io/` | URL | URL embedded in phishing email |
| `https://letsdefwnd.io` | URL | URL visited by victim on endpoint |

---

## User / Host

| IOC | Type | Context |
|-----|------|---------|
| `Mateo` | User | User observed interacting with the phishing URL |
| `chrome.exe` | Process | Browser process used to access phishing site |

---

## Assessment

The IOC set supports a phishing incident involving domain impersonation, suspicious mail infrastructure, confirmed delivery, and confirmed victim interaction.
