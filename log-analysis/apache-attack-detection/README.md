# Apache Attack Detection

This mini-project demonstrates how to detect brute force login attempts and suspicious login activity from Apache access logs using SIEM tools like Splunk.

## 🔍 Detection Goals

- Brute force login detection (e.g., multiple 401s from same IP)
- Successful logins from new or foreign IPs
- Suspicious user-agent patterns

## 📁 Files

- `sample-logs/apache_access.log`: Sample Apache access logs
- `splunk-searches.md`: Splunk detection queries
- `detection-summary.md`: Summary of findings and incident report

## 🛠️ Tools

- Splunk (or ELK stack)
- Apache logs
- Python (optional for parsing)
