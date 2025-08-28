# Plow

I was sick and tired of moving DNS records around manually when moving domains and name servers. I finally caved in and concocted this little tool. Feed this thing a domain and it will scrape all the DNS records and cram them into a BIND-valid zone file so you can simply import *that* without fiddling with all this crap.

**Disclaimer**: The vast majority of this codebase is AI-generated.

Any and all pull requests are welcome.

## Features

- Checks A, AAAA, MX, TXT, SRV, NS, and CNAME records
- Outputs results in BIND-compatible zone file
- Automatically checks 50+ common subdomains (including single letters and numbers)
- Supports additional subdomains from file or the CLI directly
- Checks _dmarc and _domainkey subdomains

## Usage

```
Usage: plow [-q|--quick] <domain> [additional_subdomains...]
Usage: plow [-q|--quick] <domain> [@subdomains_file] [additional_subdomains...]
Options:
  -q, --quick    Skip checking common subdomains list
Examples:
  plow example.com
  plow --quick example.com
  plow example.com @subdomains.txt
  plow -q example.com api blog shop
```

## Requirements

- Bash-compatible shell
- `dig` to actually get the DNS records
- `curl` to download the common_subdomains.txt file for a broad spectrum scrape

## Installation/update

   ```bash
   wget https://raw.githubusercontent.com/superDuperCyberTechno/plow/refs/heads/main/plow && chmod +x plow && sudo mv plow /usr/local/bin
   ```
