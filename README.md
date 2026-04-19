# 🔐 Network Traffic Analysis using Wireshark 
## 📌 Objective
Capture and analyze network traffic and correlate it with system-level logs to identify process-level network activity.

## 🛠️ Tools Used
- Wireshark
- Sysmon
- Windows Event Viewer

## ⚙️ Methodology
1. Captured live traffic using Wireshark
2. Filtered DNS/HTTP traffic
3. Monitored Event ID 3 logs in Sysmon
4. Correlated destination IPs with processes

## 🔍 Findings
- Observed DNS queries to domains like google.com
- Identified outbound HTTPS connections
- Mapped traffic to processes such as `comet.exe`
- Detected repeated DNS queries during browsing

## 🔗 Correlation Example
Wireshark (DNS → google.com → IP)  
↔  
Sysmon (Event ID 3 → same IP → comet.exe)

## 🛡️ Remediation
- Block suspicious domains/IPs
- Monitor processes generating network traffic
- Use SIEM for centralized logging
- Apply system updates and endpoint protection

## 📸 Screenshots
(see `/screenshots`)

## 📂 Files
- `report/` → detailed report  
- `screenshots/` → evidence  
- `sample_logs/` → optional PCAP  

## 🎯 Outcome
Demonstrated correlation of network and endpoint telemetry for basic incident analysis.
