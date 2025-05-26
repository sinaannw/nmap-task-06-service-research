# Task 06 - Research Common Services on Open Ports

## ✅ What I Did
- Reviewed the open ports discovered in previous Nmap scans.
- Researched the typical services that run on those ports.
- Noted how these services work, what they’re used for, and their common vulnerabilities.

---

## 🔍 Port and Service Summary

| Port | Service        | Description                                  | Common Risks / Notes                             |
|------|----------------|----------------------------------------------|--------------------------------------------------|
| 21   | FTP            | File Transfer Protocol                       | Unencrypted credentials, often exploited         |
| 22   | SSH            | Secure Shell                                 | Brute-force attacks, outdated version exploits   |
| 53   | DNS            | Domain Name System                           | Amplification attacks, zone transfer leaks       |
| 80   | HTTP           | Web traffic (insecure)                       | XSS, injection, MITM if not redirected to HTTPS  |
| 443  | HTTPS          | Secure web traffic (TLS/SSL)                 | TLS downgrade, expired/invalid certs             |
| 8000 | HTTP-alt       | Dev/testing web servers                      | Often unprotected or outdated                    |
| 8089 | Splunk Web     | Used by Splunk for web UI                    | Exposed log data or dashboards                   |
| 49152| Dynamic port   | Likely used by internal services or apps     | Unknown, could be RPC or P2P related             |
| 62078| iPhone sync    | Apple’s usbmuxd (for device communication)   | Shouldn’t be exposed to the open network         |

---

## 📚 Sources Used

- [Nmap Port Database](https://nmap.org/nsedoc/)
- [SpeedGuide.net Port Reference](https://www.speedguide.net/port.php)
- CVE Search and service-specific documentation

---

## 📌 Notes
- Researching the purpose of each port helps understand the services running on a network.
- Identifying risky or unnecessary ports can help prioritize what to close or secure.
