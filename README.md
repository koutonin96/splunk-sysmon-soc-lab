# splunk-sysmon-soc-lab
Security Operations Center (SOC) lab project focused on SIEM deployment, Sysmon logging, and endpoint monitoring using Splunk Enterprise.

# Splunk SOC Home Lab with Sysmon Monitoring
## Overview
This project demonstrates the setup of a Security Operations Center (SOC) home lab using Splunk Enterprise, Sysmon, and Splunk Universal Forwarder to collect, forward, and analyze Windows endpoint telemetry.

The lab simulates a real-world SOC environment where endpoint activity is monitored and centralized into a SIEM platform for security analysis and threat detection.

# Lab Architecture
| Machine       | Role                           |
| ------------- | ------------------------------ |
| Ubuntu Server | Splunk Enterprise SIEM         |
| Windows 11    | Endpoint monitored with Sysmon |
| Kali Linux    | Attacker machine for testing   |

# Technologies Used
Splunk Enterprise 10.2.3
Splunk Universal Forwarder
Sysmon
Ubuntu Linux
Windows 11
Kali Linux
VirtualBox

# Project Objectives
Install and configure Splunk Enterprise on Ubuntu
Configure Splunk Universal Forwarder on Windows 11
Install and configure Sysmon for endpoint telemetry
Forward Windows logs and Sysmon events to Splunk
Monitor process creation events
Analyze logs using SPL searches
Build a beginner SOC analyst home lab

# System Configuration

Configured Sysmon Operational logs using:

[WinEventLog://Microsoft-Windows-Sysmon/Operational]
disabled = 0
start_from = oldest
current_only = 0

# Splunk Searches
index=* EventID=1

# PowerShell Activity
index=* powershell

# Login Attempts Failed
index=* EventCode=4625

# Network Connections
index=* EventID=3

# Example Detected Events
Process execution monitoring
PowerShell activity
Windows authentication logs
Network connection events
Command execution visibility

# Challenges Encountered
During the setup, several troubleshooting steps were required:

Resolving Splunk Universal Forwarder connectivity issues
Correcting Sysmon WinEventLog channel configuration
Troubleshooting missing Sysmon logs in Splunk
Resetting fishbucket cache
Configuring proper event forwarding between Windows and Ubuntu VMs

This process improved troubleshooting, log analysis, and SIEM configuration skills.

# Screenshots
## Sysmon Events Successfully Ingested into Splunk

images/sysmon_events.png

## Splunk Data Summary

images/Data_summary.png
images/Data_summary_all_events.png

## Splunk Dashboard

images/Splunk_Dashboard_1.png
images/Splunk_Dashboard_2.png
images/Splunk_Dashboard_3.png


# Skills Demonstrated
SIEM Deployment
Security Monitoring
Windows Event Logging
Endpoint Telemetry
Splunk Administration
Log Analysis
Cybersecurity Troubleshooting
SOC Operations
Threat Detection Fundamentals

# Future Improvements
Create Splunk dashboards
Add Sigma detection rules
Integrate Suricata IDS
Simulate attacks from Kali Linux
Develop custom alerts
Add MITRE ATT&CK mappings

# Author

Adjoa Koutonin
Cyber ​​Operations Student | SOC Analyst Enthusiast | CompTIA A+ Certified
