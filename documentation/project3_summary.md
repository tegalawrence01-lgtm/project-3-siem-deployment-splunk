# Project 3: SIEM Deployment Using Splunk

## Project Summary

This project involved deploying a small SIEM environment using Splunk Cloud, a Windows endpoint, and an Ubuntu Linux virtual machine.

The purpose was to collect security logs, simulate controlled security events, and investigate the resulting activity using Splunk.

## Lab Environment

- Splunk Cloud
- Windows endpoint with Splunk Universal Forwarder
- Ubuntu Server with Splunk Universal Forwarder
- Oracle VirtualBox
- Splunk Search Processing Language (SPL)

## Security Tests

### Attack 1 — SSH Brute-Force Simulation

Controlled failed SSH login attempts were generated against the Ubuntu lab system.

Splunk was used to identify the failed authentication events and detect repeated attempts.

**MITRE ATT&CK:** T1110.001 — Password Guessing

### Attack 2 — Unauthorized Local Administrator Account

A temporary local Windows account was created and added to the local Administrators group.

Windows Security events were collected and investigated in Splunk.

The temporary account was removed after testing.

**MITRE ATT&CK:** T1136.001 — Create Account: Local Account

### Attack 3 — Controlled PowerShell Activity

Harmless PowerShell commands were executed in the Windows lab environment.

PowerShell Operational Event ID 4104 was collected and searched in Splunk to confirm the activity.

**MITRE ATT&CK:** T1059.001 — PowerShell

## Detection and Investigation

The three security tests were investigated using SPL searches in Splunk Cloud.

The final investigation combined evidence from Windows and Ubuntu and allowed the three controlled activities to be viewed together.

## Key Results

- Confirmed Windows and Ubuntu logs were reaching Splunk Cloud.
- Detected repeated failed SSH authentication attempts.
- Detected local administrator account creation activity.
- Detected controlled PowerShell activity.
- Mapped the observed activities to MITRE ATT&CK techniques.

## Evidence

Supporting screenshots are stored in the `screenshots/` directory.

Detection queries are stored in the `queries/` directory.

## Project Note

This project was completed in a controlled lab environment for educational purposes. No real systems were targeted.
