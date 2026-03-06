# Attack Simulation

This section explains the activities performed on the Windows endpoint to generate security alerts.

## 1. Account Creation

A new user account was created on the Windows system.

Command used:

net user attacker Password123 /add

Wazuh detected this activity and generated an alert for user account creation.

## 2. Privilege Escalation

The created account was added to the administrators group.

Command used:

net localgroup administrators attacker /add

This triggered alerts related to privilege escalation.

## 3. File Integrity Monitoring Test

A monitored folder was created:

C:\soc-monitor

Files were created and modified inside this folder to generate File Integrity Monitoring alerts.

Example command:

echo test > C:\soc-monitor\test.txt

Wazuh detected file creation and modification events in the monitored directory.
