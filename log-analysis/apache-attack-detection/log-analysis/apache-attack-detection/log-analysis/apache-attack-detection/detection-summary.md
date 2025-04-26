## Incident Summary

On [Date], Apache logs revealed multiple brute force login attempts originating from the IP `203.0.113.99`. Over 50 failed login attempts occurred within 3 minutes. Additionally, successful logins from previously unseen foreign IPs were detected.

## Mitigation

- Block IP `203.0.113.99` at the firewall
- Reset affected user credentials
- Enable MFA on all login endpoints
- Begin user education campaign on password hygiene

