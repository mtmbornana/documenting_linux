# Network Reconnaissance Log: scanme.nmap.org

## Overview
This documents basic network reconnaissance performed against `scanme.nmap.org` as part of entry-level Linux and cybersecurity training. 

### Lab Environment
- **Operating System:** Kali Linux
- **Virtualization:** Oracle VirtualBox
- **Purpose:** Isolated testing environment for running security tools and capturing evidence.

> **Disclaimer:** All scanning activities were conducted strictly against `scanme.nmap.org`, an authorized target provided by the Nmap Project for testing and educational purposes.

---

## Tools & Methodology

### 1. Domain Registration Query (`whois`)
- **Objective:** Gather domain registrar data and administrative details.
- **Command Used:** `whois scanme.nmap.org > owner_info.txt`
- **Output File:** [`owner_info.txt`](./owner_info.txt)

### 2. Network Port Discovery (`nmap`)
- **Objective:** Identify active services and open network ports on the target host.
- **Command Used:** `nmap scanme.nmap.org > open_doors.txt`
- **Output File:** [`open_doors.txt`](./open_doors.txt)

### 3. Data Transfer via Python Web Server (`http.server`)
- **Objective:** Transfer evidence logs out of the Kali Linux VirtualBox VM to the host environment.
- **Commands Used:** 
  - `python3 -m http.server 8000`
  - `hostname -I`
- **Methodology:** Hosted a temporary local web service inside Kali to download logs remotely via the host browser.

---

## Key Findings Summary

- **Target IP / Host:** `scanme.nmap.org`
- **Discovered Services:**
  - `22/tcp` (SSH) — Remote command line access.
  - `80/tcp` (HTTP) — Standard web service.

---

## Technical Skills Demonstrated
- Virtualization management (running Kali Linux in VirtualBox).
- Linux terminal navigation and output redirection (`>`).
- Passive information gathering via WHOIS queries.
- Active host scanning using Nmap.
- Ad-hoc file transfers using Python HTTP web servers.
- Professional documentation and log management.
