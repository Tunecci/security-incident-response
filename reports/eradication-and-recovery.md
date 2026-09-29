# Eradication and Recovery

## Objective

The objective of eradication is to remove the cause and persistence of the suspected account compromise. Recovery focuses on safely restoring the affected account and services to normal operation.

## Eradication Actions

### 1. Reset the Affected Credentials

Reset the password for `john.smith` and ensure that the new credential is unique and securely managed.

### 2. Revoke Existing Sessions

Invalidate active sessions, authentication tokens, and other credentials associated with the affected account.

### 3. Verify MFA Configuration

Confirm that MFA is enabled and that no unauthorized authentication methods, devices, or recovery options were added.

### 4. Review Account Changes

Investigate the password change at 09:16:44 and review other account-security changes for unauthorized modifications.

### 5. Investigate Endpoint Activity

Review the affected user's endpoint for signs of malware, unauthorized software, suspicious processes, or credential theft.

### 6. Review Additional Access

Search available logs for other files, systems, or services accessed by `john.smith` during the suspicious period.

### 7. Investigate Related Indicators

Search security infrastructure for activity associated with `185.220.101.14` and determine whether similar activity affected other accounts.

## Recovery Actions

### 1. Restore Account Access

After investigation and credential remediation, restore `john.smith` access using the organization's normal account-recovery process.

### 2. Monitor the Account

Place the account under increased monitoring for additional suspicious authentication attempts or unusual activity.

### 3. Validate Business Operations

Confirm that the user can access required systems normally and that security controls remain active.

### 4. Assess Customer Data Exposure

Determine the contents and sensitivity of `customer_records.csv` and investigate whether additional customer records were accessed.

The available logs confirm a successful download but do not establish whether the information was subsequently used, modified, or externally disclosed.

### 5. Document the Incident

Record the investigation, actions taken, evidence reviewed, and final findings for future security improvements and compliance requirements.

## Recovery Validation

Before considering the incident resolved, verify that:

- The compromised credentials have been reset.
- Existing sessions and tokens have been revoked.
- MFA is correctly configured.
- No unauthorized account changes remain.
- No additional suspicious access has been identified.
- Relevant evidence has been preserved.
- Customer-data exposure has been assessed.
- Monitoring is in place for recurring activity.

## Final Status

The simulated incident can be considered contained and recovered only after the above validation activities have been completed.

Further investigation would be required to determine the original source of the credentials and whether any customer information was actually disclosed outside the environment.
