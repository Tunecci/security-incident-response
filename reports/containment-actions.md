# Containment Actions

## Objective

The objective of containment is to prevent further unauthorized access while preserving evidence needed for investigation.

## Recommended Immediate Actions

### 1. Disable or Lock the Affected Account

Temporarily disable `john.smith` to prevent further unauthorized authentication while the account is investigated.

### 2. Revoke Active Sessions

Terminate active sessions and invalidate authentication tokens associated with the affected account.

### 3. Force a Credential Reset

Require a secure password reset before restoring the account.

### 4. Enable or Enforce MFA

Require multi-factor authentication for the affected account and verify that MFA has not been modified or bypassed.

### 5. Investigate the Suspicious IP

Review firewall, VPN, identity-provider, endpoint, and other available security logs for activity associated with `185.220.101.14`.

The IP should be treated as an indicator of potentially suspicious activity rather than proof of the attacker's identity.

### 6. Preserve Evidence

Preserve authentication logs, file-access logs, endpoint information, timestamps, and other relevant evidence before making changes that could destroy or alter investigative data.

### 7. Investigate Customer Data Access

Determine what information was contained in `customer_records.csv` and review additional file-access activity associated with the affected account.

### 8. Check for Additional Compromised Accounts

Search security logs for similar authentication patterns involving other accounts.

## Containment Status

For this simulated investigation, the actions above represent recommended containment measures. No real user accounts, systems, or network infrastructure were modified.

## Priority

The incident should be treated as a high-priority security investigation because the available evidence indicates possible account compromise and confirmed access to a customer-record file.
