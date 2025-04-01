# Red vs Blue: Cyber Range Simulation

## Overview
A self-contained, virtualized cyber range built from scratch on UTM with three machines simulating Red Team and Blue Team workflows.

## Purpose
To develop and demonstrate proficiency in network segmentation, threat simulation, log analysis, and adversary detection using only open-source tools in a home lab setting.

## Architecture
- **Kali-Attacker**: Launches reconnaissance, stealth scanning, and future exploitation.
- **Ubuntu-Defender**: Detects attacks via `auditd`, `rsyslog`, and UFW firewall rules.
- **Ubuntu-C2 (Planned)**: Future command-and-control server using Sliver or Metasploit.

## Tools Used
- **Nmap** (Kali) - for stealth TCP SYN scanning
- **auditd** (Defender) - for command monitoring and user activity
- **rsyslog** (Defender) - for centralized system logging
- **UFW** - for logging and blocking unauthorized inbound scans
- **UTM (QEMU)** - for VM management on Apple Silicon

## Simulated Scenario
1. Kali-Attacker scans the Defender's IP using:
    ```bash
    sudo nmap -sS 192.168.64.8
    ```
2. Defender logs and blocks TCP SYN requests via:
    ```bash
    tail -f /var/log/syslog
    ```
3. Attack origin is confirmed using MAC and IP metadata in UFW kernel logs.

## Skills Demonstrated
- Network isolation and static IP configuration
- Red Team recon via Nmap
- Blue Team visibility using syslog and audit logs
- Manual correlation of scan traffic with firewall logs

## Screenshots
- [ ] UFW logs showing blocked scans
- [ ] Network map (Kali ↔ Ubuntu Defender)

## Future Expansion
- Add Sliver or Metasploit to Ubuntu-C2 VM
- Integrate Filebeat + Kibana for visual log dashboards
- Simulate lateral movement or privilege escalation scenarios

---

**Tags:** #CyberSecurity #RedTeam #BlueTeam #DetectionEngineering #Linux #HomeLab
