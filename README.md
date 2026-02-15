# Start

This repository is the baseline for my technical aspirations. It serves as a living record of the tools, frameworks, and architectures I am mastering to build resilient, high-performance systems.

## Current Project: OCI Unkillable Node
The first milestone is the "Oracle Defender"—a Go-based systems tool designed to ensure Always-Free instances remain active by satisfying strict resource utilization requirements.

### Quick Start (Defender Operations)
- **Check Status:** `systemctl status defender`
- **View Logs:** `journalctl -u defender -f`
- **Update/Rebuild:**
  ```bash
  go build -o /usr/bin/defender main.go && \
  chmod +x /usr/bin/defender && \
  restorecon -v /usr/bin/defender && \
  systemctl restart defender
