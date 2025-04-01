Linux Host-Based Detection Using auditd & syslog
Overview
A lightweight host-based detection stack built without commercial tooling. Uses native Linux utilities to monitor, log, and alert on suspicious activity.

Why It Matters
Security doesn’t require expensive tools — it requires visibility. This setup proves that even on an ARM virtual machine, you can build a functional detection system using only Linux internals.

What It Does
Tracks command execution with auditd

Monitors privileged actions (e.g., sudo, service restarts)

Captures system events using rsyslog

Allows real-time analysis with tail, grep, ausearch

Employer Relevance
Demonstrates Blue Team fundamentals on Linux

Prepares for SIEM integration (e.g. Filebeat → ELK)

Useful for endpoint logging policies and detection engineering
