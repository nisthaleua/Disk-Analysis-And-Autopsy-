# Disk Analysis and Autopsy: Digital Forensics Investigation

A forensic investigation of a compromised Windows system, carried out by analysing an **E01 disk image in Autopsy**. The goal was to reconstruct system activity, find attacker traces and document the evidence step by step.

> Guided forensics lab on **TryHackMe**, completed as part of my project internship at Threat Prism (1stop.ai), Jan–Mar 2026.

## Report

📄 **[report.pdf](report.pdf)** (20 pages: case setup, 12 investigation steps with screenshots, evidence summary table)

## Scope

- Analyse an E01 disk image and verify its integrity
- Identify system details, user accounts and recent activity
- Extract network artifacts and browsing evidence
- Detect attacker tools and exploit traces

## Tools

Autopsy · E01 forensic image · Windows registry and artifact analysis

## Investigation Walkthrough

| # | Step | What was done |
|---|---|---|
| 1 | Case creation and image loading | Created an Autopsy case and loaded the E01 image with ingest modules enabled |
| 2 | Hash verification | Located the MD5 hash in the image metadata to confirm integrity |
| 3 | System information | Identified the computer name |
| 4 | User accounts | Listed all user accounts |
| 5 | Last login | Determined the most recently active user from timestamps |
| 6 | Network information | Extracted IP and MAC address from registry paths and configuration files |
| 7 | Network card | Identified the network adapter from the Windows registry |
| 8 | Web activity | Reviewed bookmarks and accessed URLs/IPs |
| 9 | User data | Confirmed user identity from Desktop contents |
| 10 | PowerShell history | Recovered evidence from the user's PowerShell command history |
| 11 | Hacking tools | Found **Mimikatz**, **Lassen** (via Prefetch) and **Yara** in Downloads and Prefetch artifacts |
| 12 | Exploit identification | Located a **Zerologon** exploit archive among recent documents |

## Skills Demonstrated

- Evidence handling and integrity verification (hashing)
- Windows artifact analysis: registry, Prefetch, PowerShell history, user data
- Reconstructing an attack timeline from disk evidence
- Writing a clear, evidence-backed forensic report

## Repository Contents

```
├── README.md
└── report.pdf      # Full forensic report
```

## Note

The disk image comes from a TryHackMe training room and is not included in this repository.
