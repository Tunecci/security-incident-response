# Incident Timeline

## Overview

The following timeline documents authentication and file-access events associated with the affected account, `john.smith`.

| Time | Event | Source IP | Assessment |
|---|---|---|---|
| 08:41:12 | Successful login | 192.168.1.45 | Normal baseline activity |
| 09:14:03 | Failed login | 185.220.101.14 | Suspicious |
| 09:14:08 | Failed login | 185.220.101.14 | Suspicious |
| 09:14:15 | Failed login | 185.220.101.14 | Suspicious |
| 09:14:23 | Failed login | 185.220.101.14 | Suspicious |
| 09:14:31 | Failed login | 185.220.101.14 | Suspicious |
| 09:15:02 | Successful login | 185.220.101.14 | Suspicious authentication |
| 09:16:44 | Password change | 185.220.101.14 | Potential account takeover indicator |
| 09:18:21 | Customer records downloaded | 185.220.101.14 | Potential data exposure |
| 09:21:07 | Successful login | 185.220.101.14 | Continued suspicious access |
| 09:25:42 | Failed login | 192.168.1.45 | Isolated failure from known source |

## Suspicious Activity Pattern

The investigation identified the following sequence:

**Five failed login attempts → successful authentication → password change → customer records download → continued successful access.**

The repeated failed attempts occurred within approximately 28 seconds and originated from the same unusual external IP address.

The subsequent password change and access to `customer_records.csv` increased the significance of the authentication activity.

## Distinguishing Suspicious Activity from Normal Errors

Not every failed login was treated as malicious.

The failed login at 09:25:42 originated from `192.168.1.45`, an IP previously associated with a successful login by the same user. It was also an isolated failure.

In contrast, the activity from `185.220.101.14` involved multiple rapid authentication failures followed by successful authentication, a password change, and access to customer records.

The assessment was therefore based on the **frequency, timing, source, sequence, and related post-authentication activity**, rather than on failed login events alone.

## Initial Assessment

The evidence is consistent with a possible compromise of the `john.smith` account.

The logs confirm successful authentication and a customer-record download from the suspicious source. However, the logs alone do not establish whether the downloaded data was subsequently used, modified, or externally disclosed.
