# Splunk-Security-Monitoring-Projects
# Splunk Fundamentals

## Overview

This project focuses on learning the fundamentals of Splunk, a powerful SIEM (Security Information and Event Management) and log analysis platform used for monitoring, searching, analyzing, and visualizing machine-generated data.

The purpose of this project is to gain practical knowledge of Splunk basics, log ingestion, SPL queries, dashboards, and alerts for cybersecurity monitoring.

---

## Objectives

- Understand Splunk fundamentals
- Learn log ingestion process
- Analyze Linux authentication logs
- Practice SPL (Search Processing Language)
- Create dashboards and alerts
- Monitor security-related events

---

## Tools Used

- Splunk Enterprise
- Ubuntu Linux
- OpenSSH Server
- Linux Authentication Logs (`auth.log`)
- Splunk Universal Forwarder

---

## Lab Setup

### Environment

| Machine | Purpose |
|----------|----------|
| Ubuntu VM | Splunk Server |
| Linux Logs | Authentication Monitoring |
| Universal Forwarder | Log Collection |

---

## Features Practiced

### 1. Log Monitoring
Monitoring Linux authentication logs using Splunk.

**Log File:**

```bash
/var/log/auth.log
````

---

### 2. Data Ingestion

Logs were added into Splunk using:

* Upload Method
* Monitor Files
* Universal Forwarder

---

### 3. SPL Queries

#### Show All Logs

```spl
index=main
```

#### View Authentication Logs

```spl
index=main source="/var/log/auth.log"
```

#### Count Total Events

```spl
index=main
| stats count
```

#### View Top Sources

```spl
index=main
| top source
```

---

### 4. Dashboard Creation

Created dashboards for:

* Login Monitoring
* Failed Authentication Events
* Security Event Visualization
* Log Statistics

---

### 5. Alert Creation

Configured alerts for:

* Multiple Failed Login Attempts
* Suspicious Authentication Events
* Brute Force Detection

Example Query:

```spl
index=main "Failed password"
| stats count
| where count > 3
```

---

## Learning Outcomes

Through this project, I learned:

* Splunk installation and setup
* Log ingestion techniques
* SPL query writing
* Linux authentication log analysis
* Dashboard creation
* Alert configuration
* Basic security monitoring

---

## Project Outcome

This project helped me build a strong foundation in Splunk and understand how SIEM tools are used for cybersecurity monitoring and log analysis.

---

## Author

**Aravinth R**
Cybersecurity Enthusiast | SOC Analyst Learner

```
```
