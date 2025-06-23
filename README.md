# local-network-port-scan
Scan your local network for open ports using Nmap
# Network Port Scan Report

Objective : 
Scan the local network (`192.168.*.1/24`) for open ports to identify services and potential security risks.

Scan Summary : 
Tool: Nmap 7.97  
Scan Type: TCP SYN (`nmap -sS`)

Open Ports Found:
| Port  | Service             | Notes                         |
|--------|--------------------|-------------------------------|
| 80     | HTTP               | Web service (unencrypted)     |
| 135    | MSRPC              | Windows RPC                   |
| 139    | NetBIOS-SSN        | Windows file sharing           |
| 443    | HTTPS              | Secure web service             |
| 445    | Microsoft-DS       | SMB file sharing               |
| 1025   | NFS-or-IIS         | Dynamic Windows service        |
| 3306   | MySQL              | Database service               |
| 6881   | BitTorrent Tracker | P2P file sharing               |
| 7070   | RealServer         | Streaming service              |

Risks & Actions
- Some ports expose file sharing and databases.
- Applied Windows Firewall to block unused ports.
- Reviewed processes using `netstat -ano` for further security.

Included
- `scan_results.txt` — Nmap output
- `Task 1.docx` — Scan summary and findings

---

Completed by Sairam Dvns. 
