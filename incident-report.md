# Incident Report: Repeated Failed Login Attempts

## Summary
This report reviews authentication log data to identify suspicious repeated failed login attempts from external IP addresses.

## Objective
The goal was to detect potential brute-force behavior by analyzing failed SSH login activity and identifying IP addresses that exceeded a chosen alert threshold.

## Data Source
Sample authentication log reviewed with a Python log analysis script.

## Tools Used
- Python
- Regular expressions
- CSV export
- Terminal

## Method
1. Parsed log entries for failed password attempts
2. Extracted source IP addresses
3. Counted repeated failures by IP
4. Flagged IPs with 3 or more failed attempts

## Findings
The following IP addresses met the alert threshold:
- 192.168.1.10
- 10.0.0.5

## Interpretation
Repeated failed login attempts from the same source may indicate password guessing, unauthorized access attempts, or a misconfigured service account.

## Recommended Next Steps
- Review authentication activity for affected accounts
- Block or rate-limit suspicious IP addresses
- Enable stronger authentication controls
- Expand monitoring to additional log sources

## Lessons Learned
This exercise reinforced the value of log analysis, scripting for security automation, and clear documentation of findings.
