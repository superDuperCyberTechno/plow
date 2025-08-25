# Plow

A bash script to check DNS records for a domain and its subdomains, outputting results in BIND zone file format.

## Features

- Checks all common DNS record types: A, AAAA, MX, TXT, SRV, NS, and CNAME
- Outputs results in BIND-compatible zone file format
- Automatically checks 50+ common subdomains (including single letters and numbers)
- Supports additional subdomains from file or command line
- Optimized to skip unnecessary checks for CNAME records

## Requirements

- Bash shell
- `dig` command (from bind-utils package)

## Installation

1. Save the script as `dns_check.sh`
2. Make it executable:
   ```bash
   chmod +x dns_check.sh
