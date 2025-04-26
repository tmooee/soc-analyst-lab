# 📝 Detection Summary – Apache Log Analysis

## 🔍 Incident Overview

On April 26, 2025, Apache access logs indicated two distinct suspicious activities:

1. **Brute Force Attempt**  
   - IP: `192.168.1.10`  
   - 5 failed logins (401) followed by a successful login (200)

2. **Suspicious Tool Usage**  
   - IP: `203.0.113.99`  
   - 4 failed logins and 1 success using `curl/7.58.0` as User-Agent

3. **Probing of Sensitive Endpoint**  
   - IP: `198.51.100.77`  
   - Attempted access to `/wp-login.php` using `sqlmap`

---

## ✅ Recommended Actions

- 🚫 Block `203.0.113.99` and `198.51.100.77` at the firewall
- 🔐 Enforce Multi-Factor Authentication (MFA)
- 🔄 Reset passwords for affected users
- 🔍 Continue monitoring for further activity from similar IPs and tools
