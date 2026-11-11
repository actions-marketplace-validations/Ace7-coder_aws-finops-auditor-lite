# AWS FinOps Auditor (Lite)

A lightweight, local Python CLI tool designed to detect orphaned AWS resources and identify hidden infrastructure waste before it compounds into financial debt.

This repository contains the **free community edition** for analyzing basic AWS usage and billing exports.

---

### Edition Comparison

| Capability | Lite (Community) | Consultant & MSP Toolkit |
| :--- | :---: | :---: |
| Single-Account CSV Analysis | Yes | Yes |
| Orphaned Storage & Idle Compute Detection | Yes | Yes |
| Local Terminal & JSON Output | Yes | Yes |
| AWS Organizations Multi-Account Scanning (`sts:AssumeRole`) | No | **Yes** |
| Client-Ready Showback Reports (Markdown & PDF) | No | **Yes** |
| Automated 1-Click Remediation Scripts (`--remediate`) | No | **Yes** |
| Commercial Assessment License (Agency/Client Rights) | No | **Yes** |

👉 **[Get the Consultant & MSP Toolkit on Gumroad](https://aisser.gumroad.com/l/krgac)** *(Practitioner $99 / Agency Pack $499)*

---

## 🚀 Commercial Editions: Consultant & MSP Toolkit

Built for cloud consultants, MSPs, and infrastructure teams managing multi-account environments. The commercial toolkit shifts from static single-account file analysis to automated multi-account discovery and client-facing deliverables.

- **AWS Organizations Multi-Account Engine:** Automatically discovers and assumes cross-account IAM roles across all member accounts in your AWS Organization.
- **Client-Ready Showback Reports:** Generates executive Markdown and PDF summaries with showback by department and annualized savings calculations.
- **1-Click Remediation Generator:** Auto-generates idempotent remediation scripts (`remediate_anomalies.sh`) for pull request review before deletion.
- **Commercial Assessment Rights:** Includes a formal agency license permitting paid client assessments and audits.

👉 **[Download the Commercial Toolkit](https://aisser.gumroad.com/l/krgac)**

---

## Lite Version Overview

The free Lite engine executes multi-vector cost and anomaly calculations locally against exported AWS billing or usage CSV files. It flags:
- **Unattached EBS Volumes:** Identifies detached `gp2`, `gp3`, and `io2` storage incurring baseline monthly costs.
- **Idle EC2 Instances:** Flags active compute instances running at sub-5% average CPU utilization.
- **Unassociated Elastic IPs:** Catches unattached public IPv4 addresses incurring hourly reservation fees.
- **Security & Configuration Anomalies:** Identifies unencrypted volumes and internet-exposed endpoints.

### Quickstart

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Ace7-coder/aws-finops-auditor-lite.git](https://github.com/Ace7-coder/aws-finops-auditor-lite.git)
   cd aws-finops-auditor-lite