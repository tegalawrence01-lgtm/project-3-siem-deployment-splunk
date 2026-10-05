# Project 3: SIEM Deployment Using Splunk

## Project Overview

This project involved setting up a Security Information and Event Management (SIEM) environment using Splunk Cloud, a Windows endpoint, and an Ubuntu Linux virtual machine.

The aim was to collect security logs, simulate controlled security events, and use Splunk searches to identify and investigate those events.

## Objectives

- Configure Splunk Universal Forwarders on Windows and Ubuntu.
- Send endpoint logs to Splunk Cloud.
- Monitor Windows and Linux security events.
- Perform controlled security simulations.
- Investigate collected events using SPL.
- Map observed activity to the MITRE ATT&CK framework.

## Lab Environment

- **SIEM:** Splunk Cloud
- **Windows endpoint:** Windows with Splunk Universal Forwarder
- **Linux endpoint:** Ubuntu Server with Splunk Universal Forwarder
- **Virtualization:** Oracle VirtualBox
- **Log analysis:** Splunk Search Processing Language (SPL)

## Security Tests

### 1. SSH Brute-Force Simulation

Generated controlled failed SSH login attempts against the Ubuntu lab system and searched for the resulting security events in Splunk.

### 2. Unauthorized Administrator Account

Created a temporary local Windows account, added it to the Administrators group, and investigated the related Windows Security events.

The temporary account was removed after testing.

### 3. Controlled PowerShell Activity

Ran harmless PowerShell commands in the Windows lab environment and searched for the corresponding PowerShell Operational events.

## Key Results

- Confirmed Windows and Ubuntu logs were reaching Splunk Cloud.
- Detected failed SSH login attempts.
- Investigated Windows account creation and administrator-group membership events.
- Captured controlled PowerShell activity using Windows Event ID 4104.
- Combined evidence from the three tests in a Splunk investigation.

## Skills Demonstrated

- SIEM deployment and configuration
- Windows and Linux log collection
- Security event analysis
- SPL searching and filtering
- Basic incident investigation
- MITRE ATT&CK mapping
- Security documentation

## Evidence

Screenshots and supporting project documentation will be added to this repository.

## Disclaimer

This project was completed in a controlled lab for educational purposes. No real systems were targeted.
