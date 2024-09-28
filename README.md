# Taskseven - Security Scans on Metasploitable VM

## Overview

This project contains security assessments performed on the **Metasploitable VM**. The following tools were used for the assessments:
1. **Nessus**: Vulnerability scanning and reporting.
2. **Nikto**: Web server vulnerability scanning.
3. **Netcat**: Banner grabbing from open ports.

The results from these assessments are included in this repository in the `Taskseven` folder.

---

## Contents

1. **Nessus Report (PDF)**: A detailed vulnerability scan performed on the Metasploitable VM.
2. **Nikto Report (HTML)**: A web server vulnerability scan performed on the Metasploitable VM using Nikto.
3. **Netcat Banner Screenshot (PNG)**: A screenshot capturing the banner information retrieved from an open FTP port (port 21) using Netcat.

---

## Steps Performed

### 1. Nessus Scan
1. **Open Nessus** and log in.
2. Create a new **Basic Network Scan** targeting the IP address `10.0.2.4` of the Metasploitable VM.
3. Start the scan and wait for the results.
4. After the scan completes, export the report as a **PDF** and save it.
5. The generated PDF file is named `nessus_report.pdf`.

### 2. Nikto Scan
1. **Run Nikto** in a terminal using the command:
   ```bash
   nikto -h 10.0.2.4 -o nikto_report.html -Format html

2. This generates a vulnerability report of the web server running on the Metasploitable VM.
3. The generated report is saved as ```nikto_report.html.```

### 3. Netcat Banner Grabbing
1. Use Netcat to connect to the FTP service running on port 21 of the Metasploitable VM:
```nc 10.0.2.4 21```
2. This returns the banner of the FTP service (vsFTPd 2.3.4).
3. A screenshot of the banner output is taken and saved as netcat_banner.png.
