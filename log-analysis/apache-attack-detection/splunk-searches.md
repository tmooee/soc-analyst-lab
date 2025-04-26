# Splunk Detection Queries – Apache Access Logs

This file contains detection queries for identifying suspicious activity in Apache web server access logs using Splunk.

---

## 🔐 Brute Force Login Attempt Detection

Detect repeated failed login attempts (HTTP 401 errors) from the same IP address.

```spl
sourcetype=apache_access status=401 
| stats count by src_ip 
| where count > 10
sourcetype=apache_access status=200 uri="/login"
| stats earliest(_time) as first_seen by src_ip, user
| where first_seen > relative_time(now(), "-1d")
sourcetype=apache_access 
| search user_agent="curl/*" OR user_agent="Python-urllib/*" OR user_agent="sqlmap" OR user_agent="nmap"
| stats count by src_ip, user_agent

---

✅ You can now paste that **entire block** into your `log-analysis/apache-attack-detection/splunk-searches.md` file.

Want the `apache_access.log` next?
