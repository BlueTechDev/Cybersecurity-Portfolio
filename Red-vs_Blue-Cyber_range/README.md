1. Red vs Blue: Cyber Range Simulation
Overview
A self-contained, virtualized cyber range built from scratch on UTM with three machines simulating Red Team and Blue Team workflows.

Purpose
To develop and demonstrate proficiency in network segmentation, threat simulation, log analysis, and adversary detection — using only open-source tools and a manually configured lab.

Architecture
Kali-Attacker: Conducts stealth and active recon using Nmap

Ubuntu-Defender: Detects attacks via auditd, rsyslog, and UFW

Ubuntu-C2 (Planned): Future host for C2 framework (Sliver or Metasploit)

Key Skills Demonstrated
Red Team recon and stealth scanning (nmap -sS)

System hardening and endpoint firewall tuning (UFW)

Real-time log analysis (/var/log/syslog, ausearch)

VM networking (host-only, IP assignment, interface management)

Deliverables
Simulated TCP scan triggering UFW logs

Defender successfully blocking & logging attack attempts

Command logs from attacker and detection side-by-side
