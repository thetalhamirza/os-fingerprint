# OS Fingerprint Scanner

A Python script for OS fingerprinting and service detection using Nmap. This script scans specified ports on a target host to gather OS and service information.

## Features

- **OS Fingerprinting:** Identifies the operating system of the target host.
- **Service Detection:** Retrieves service name, product, and version for specified ports.
- **CSV Output:** Saves the scan results to a CSV file for easy analysis.

## Usage

```bash
python os-recon.py <host> -p <ports> [-o <output_file>]
```

### Parameters:

- `<host>`: The target IP address (e.g., `192.168.1.1`).
- `-p, --ports`: Comma-separated list of ports to scan (e.g., `22,80,443`).
- `-o, --output` _(optional)_: Specify the output CSV file. Defaults to `scan_results.csv`.

### Example:

```bash
python os-recon.py 192.168.1.1 -p 22,80,443 -o results.csv
```

## Requirements

- **Python 3**
- **Libraries:**
    - `python-nmap`
    - `argparse`
    - `csv`

Install dependencies with:

```bash
pip install python-nmap
```

## Example Output

```
[+] Scanning IP: 192.168.1.1
[+] Scanning ports: 22,80,443

[+] Scan Results:
IP: 192.168.1.1
OS: Linux
Port: 22
Name: ssh
Product: OpenSSH
Version: 7.4

IP: 192.168.1.1
OS: Linux
Port: 80
Name: http
Product: Apache
Version: 2.4.29
```

## Credits

Special thanks to **faanross** for the inspiring tutorial that guided the development of this script.

## License

This project is for educational and ethical use only. Always ensure you have permission before scanning networks.