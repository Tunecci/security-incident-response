# Indicators of Compromise (IOCs)

## Overview

The investigation identified several indicators associated with the suspicious activity involving the `john.smith` account.

An IOC is an observable artifact that can support the identification or investigation of potentially malicious activity. An IOC does not by itself prove the identity of an attacker.

## Identified Indicators

| Type | Indicator | Significance |
|---|---|---|
| IP Address | `185.220.101.14` | Source of repeated failed logins, successful authentication, password change, and customer-record download |
| Username | `john.smith` | Account associated with the suspicious activity |
| File | `customer_records.csv` | Customer data file successfully downloaded during the suspicious session |
| Reverse DNS | `berlin01.tor-exit.artikel10.org` | Hostname associated with the suspicious IP address |

## IP Address Investigation

The suspicious source IP was investigated using WHOIS and reverse DNS.

The IP address `185.220.101.14` was associated with a Tor exit relay registered to Artikel10 e.V. in Germany.

Because Tor can obscure the originating source of network traffic, the IP address alone cannot be used to determine the attacker's actual location or identity.

## Relevant Activity

The suspicious IP was associated with:

- Five failed login attempts against `john.smith`.
- A subsequent successful login.
- A successful password change.
- A successful download of `customer_records.csv`.
- Another successful login from the same source.

## IOC Handling Recommendations

Security teams could use these indicators to:

- Search other authentication and security logs.
- Identify related activity involving other accounts.
- Review firewall, VPN, identity-provider, and endpoint logs.
- Monitor for additional activity involving the suspicious IP.
- Investigate access to the affected customer-data file.
- Correlate the indicators with other available security telemetry.

## Important Limitation

The available evidence does not establish that `185.220.101.14` represents the attacker's physical location or personally identifies the attacker.

The IP should therefore be treated as an indicator associated with suspicious activity rather than definitive attribution.
