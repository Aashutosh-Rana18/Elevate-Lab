#port-scan-day1

Author: Aashutosh Rana
Date: 22-09-2025

Day 1 — Hands-on exploration of port scanning using Nmap and Nessus.

Table of Contents

Project Overview

Repository Layout

Tools & Methods

How to Reproduce Scans (Examples)

Outputs & Reports

Key Takeaways

Roadmap

Contributing

License

Project Overview

This repository documents Day 1 of my network reconnaissance learning journey.
The primary focus is on:

Discovering open ports

Enumerating running services

Interpreting scan results

Both Nmap (for discovery and service detection) and Nessus (for vulnerability-oriented scanning) were used.

Repository Layout
port-scan-day1/
├─ Detailed_Report.docx        # Detailed insights and observations from Day 1
├─ README.md                   # Project overview and documentation
├─ Output.docx/                # Collected scan results and images
│  ├─ nmap/                    # Nmap outputs and screenshots
│  └─ nessus/                  # Nessus reports and screenshots
└─ scripts/                    # Helper scripts (if any, optional)

Tools & Methods

Nmap — versatile network discovery and service enumeration

TCP SYN scans, service/version detection, OS detection

Nessus — advanced vulnerability scanning, including port-based assessments

Command-Line Interface (CLI) — to run and automate scans

Markdown / Word docs — for reporting and documentation

How to Reproduce Scans (Examples)

⚠️ Disclaimer: Run scans only on systems/networks you own or are authorized to test.

Nmap — Common Examples
# Quick host discovery with top 100 ports
nmap -Pn --top-ports 100 -oA output/top100 192.168.1.0/24

# Full TCP SYN scan + service/version + OS detection
nmap -sS -sV -O -p- -T4 -oN output/full_scan.txt 192.168.1.10

# Export in XML format
nmap -sS -sV -oX output/scan.xml 192.168.1.10

Nmap — Specific Checks
# Scan selected ports with NSE scripts
nmap -sV --script=banner,vuln -p 22,80,443 203.0.113.5 -oN output/target_quick.txt

Nessus — Workflow

Create a new scan (Basic Network Scan / Port Scan template) in the Nessus Web UI

Configure target IPs or ranges

Run the scan

Export results (.html, .csv, .nessus) and store under Output.docx/nessus/

Outputs & Reports

Detailed_Report.docx — summary of findings, screenshots, and analysis

Output.docx/ — raw outputs and exported reports

nmap/ → .nmap, .xml, screenshots

nessus/ → exported .nessus, .html, .pdf reports

Key Takeaways

Nmap is powerful for quick discovery, detailed enumeration, and flexible output formats.

Nessus enhances analysis by mapping services to vulnerabilities (CVEs, misconfigurations).

Documenting commands, scope, and timestamps ensures reproducibility and audit readiness.

Ethical reminder: never scan systems without explicit permission.

Roadmap

Next steps beyond Day 1:

Service-specific enumeration (HTTP, FTP, SMB, etc.)

Parsing and analyzing Nmap XML for automation

Authenticated Nessus scans for deeper insights

Comparing pre- and post-remediation vulnerability reports

Integration into vulnerability management workflows

Contributing

Want to improve this project?

Open an issue with suggestions

Submit a pull request with:

Clear description of the changes

Updated report files or new analysis
