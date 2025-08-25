# Plow

I was sick and tired of moving DNS records around manually when moving domains and name servers. I finally caved in and made this little tool. Feed this thing a domain and it will scrape all the DNS records and cram them into a BIND-valid zone file so you can simply import *that* without fiddling with all this crap.

## Features

- Checks A, AAAA, MX, TXT, SRV, NS, and CNAME records
- Outputs results in BIND-compatible zone file
- Automatically checks 50+ common subdomains (including single letters and numbers)
- Supports additional subdomains from file or the CLI directly

## Requirements

- Bash shell
- `dig` command (from bind-utils package)

## Installation

   ```bash
   wget https://raw.githubusercontent.com/superDuperCyberTechno/plow/refs/heads/main/plow && chmod +x plow && sudo mv plow /usr/local/bin
   ```
