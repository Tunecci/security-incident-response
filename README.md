# Security Incident Investigation & Incident Response

## Project Overview

This project demonstrates a simulated cybersecurity incident investigation involving a suspected compromise of a user account and potential access to customer data.

The investigation was performed using simulated security logs in a Kali Linux environment. The objective was to identify suspicious authentication activity, establish an incident timeline, analyze indicators of compromise, and develop appropriate containment, eradication, and recovery actions.

## Scenario

The security team identified unusual authentication activity involving the account `john.smith`.

The investigation focused on determining whether the activity represented normal user error or a potentially unauthorized account compromise.

### Key Evidence

- Five failed login attempts occurred within approximately 28 seconds.
- The attempts originated from `185.220.101.14`.
- A successful login followed the failed attempts.
- The password was changed shortly afterward.
- `customer_records.csv` was downloaded from the same source.
- Another successful login occurred from the same source.
- A separate failed login later originated from the user's previously observed IP address, `192.168.1.45`.

## Investigation Approach

The investigation used Linux command-line tools to analyze the simulated security logs.

### Commands Used

```bash
grep "failed" logs/security.log
grep "185.220.101.14" logs/security.log
grep "download" logs/security.log
grep "password_change" logs/security.log
grep "john.smith" logs/security.log
grep "185.220.101.14" logs/security.log | grep "user="
