# Automated-Brute-Force-Detection-Sentinel
Detection and investigation of brute-force login attempts using Microsoft Sentinel and KQL.


Automated Brute-Force Attack Detection and Alerting Using Microsoft Sentinel

1. Project Overview

Brute-force attacks are a common cybersecurity threat in which attackers repeatedly attempt to guess a user's password to gain unauthorised access to an account.

This project focuses on detecting brute-force login attempts using Microsoft Sentinel and Kusto Query Language (KQL).

Windows Security Event Logs are analysed to identify repeated failed login attempts and suspicious authentication activities. Detection rules are used to generate alerts for further SOC investigation.

2. Project Objectives

- Detect multiple failed login attempts.
- Identify suspicious authentication activities.
- Monitor successful logins following repeated failures.
- Create detection queries using KQL.
- Generate security alerts using Microsoft Sentinel.
- Understand the SOC investigation process.

3. Tools and Technologies

- Microsoft Sentinel
- Microsoft Azure
- Kusto Query Language (KQL)
- Windows Security Event Logs
- MITRE ATT&CK Framework

4. Understanding Windows Event IDs

Event ID         Description
4624             Successful login
4625             Failed login

Event ID 4625 is particularly useful for identifying repeated authentication failures.

5. Attack Detection Scenarios

Scenario 1: Multiple Failed Login Attempts

Detect five or more failed login attempts within a five-minute period.

Scenario 2: Failed Login Followed by Successful Login

Identify accounts where repeated login failures are followed by a successful login.

Scenario 3: Suspicious Authentication Activity

Investigate unusual source IP addresses, targeted accounts and repeated authentication failures.

6. Detection Logic

KQL queries are used to analyse Windows Security Event Logs and identify suspicious login patterns.

The detection logic groups failed login events by account and source IP address to identify repeated authentication failures.

See the KQL-Queries folder for the detection queries.

7. MITRE ATT&CK Mapping

- T1110 – Brute Force
- T1110.001 – Password Guessing
- T1110.003 – Password Spraying

8. SOC Investigation Process

1. Review the generated security alert.
2. Identify the affected user account.
3. Examine the source IP address.
4. Analyse failed login events.
5. Check for successful login activity.
6. Determine whether the activity is suspicious.
7. Document investigation findings.
8. Recommend appropriate response actions.

9. Project Screenshots

Screenshots of the Microsoft Sentinel workspace, KQL queries, detection results and alerts will be added here.

10. Project Outcome

This project demonstrates the use of Microsoft Sentinel and KQL for detecting suspicious authentication activity and supporting SOC incident investigation.

Disclaimer

This project is intended for educational and defensive cybersecurity purposes. Testing should be performed only in authorised lab environments.
