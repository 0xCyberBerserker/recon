```

# LAN Enumeration and Reconnaissance Tool

This project provides a structured workflow for organizing penetration testing environments and automating local network reconnaissance. It consists of two primary components:

---

## 1. Environment Creation Script

Before running any recon scans, use this script to create a new testing environment with a standardized folder structure under `~/environments`.

### Features:

* Prompts for a new environment name.
* Creates essential subdirectories for different pentesting phases:

  * `recon`
  * `lan-enum`
  * `wifi-attacks`
  * `web-testing`
  * `exploits`
  * `postex`
  * `loot`
  * `notes`
  * `tools`
  * `logs`
* Initializes basic files for notes and logs.
* Displays the created folder tree for verification.

### Example usage:

```
./create\_env.sh
```

---

## 2. Recon Script

Once an environment exists, run the recon script to automate network enumeration within that environment.

### Features:

* Interactive selection of existing environments.
* Automatic detection of the current subnet.
* Fast ping sweep to identify live hosts.
* Service/version detection on live hosts using `nmap`.
* Vulnerability lookup through `nmap` vulners script and `searchsploit`.
* Generates a detailed Markdown summary of findings within the selected environment folder.

### Example usage:

```
sudo ./recon
```

---

## Requirements

* Bash (GNU Bash 4+ recommended)
* `nmap`
* `searchsploit` (Exploit Database)
* `percol`
* `curl`
* `xmllint`
* `tree` (for environment creation script display)

Install on Debian/Ubuntu with:

```
sudo apt update
sudo apt install nmap exploitdb percol curl libxml2-utils tree
```

---

## Setup Notes

* Run the environment creation script first to initialize your workspace.
* Use `recon` with root privileges for network scans.
* Customize the scripts as needed to fit your workflow.
* Organize multiple pentest projects by creating separate environments.

---

## License

Provided as-is without warranty. Use responsibly and comply with applicable laws.

---

## Author

Developed and maintained by aesir.

---

Contributions and feedback are welcome.
```
