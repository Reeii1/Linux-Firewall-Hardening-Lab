# Linux Firewall Hardening Lab (UFW & iptables)

## Project Overview
This project demonstrates the process of hardening a Linux environment (Ubuntu Server) by designing, implementing, and validating host-based firewall policies. The lab covers transitioning from standard UFW management to granular kernel-level packet filtering using `iptables`.

## Architecture & Policy Design
The firewall is configured with a **Default-Deny** posture following the *Principle of Least Privilege*.

### Approved Security Rules:
* **SSH (Port 22):** Allowed for secure system administration.
* **HTTP/HTTPS (Ports 80/443):** Allowed for incoming web traffic.
* **DNS (Port 53 UDP):** Allowed outbound for name resolution.
* **Stateful Inspection:** Allowed traffic for existing connections (ESTABLISHED, RELATED).
* **ICMP (Ping):** Explicitly **Dropped** to hide the host from network discovery.

## Files in this Repository
* `firewall_script.sh`: The automated shell script containing all deployed `iptables` rules.
* `Firewall_Report.pdf`: Comprehensive lab report including implementation screenshots, testing logs, and security reflection questions.
