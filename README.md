# Service Desk Ticketing Simulation (Jira ITSM)

## Overview
This project was built to practise and demonstrate basic IT Support / Service Desk work using a small home lab and Jira Service Management.

The focus is on how tickets are handled day to day:
logging issues, prioritising them, troubleshooting common problems, communicating with users, and closing tickets properly once the issue is fixed.

---

## Lab Architecture
**Domain:** lab.local  
**Network:** Host-only (isolated internal network)

**Domain Controller (DC01)**
- Windows Server 2019
- IP: 192.168.100.10 (static)
- Used for Active Directory and DNS

**Client Machine (CLIENT01)**
- Windows 11
- Domain-joined
- Used to simulate end-user issues

### Network Diagram
![Lab Diagram](diagram.png)

---

## Portal Design Improvement
The self-service portal was redesigned to:
- Remove duplicate “Get IT help” options
- Centralise login/account issues
- Reduce incorrect ticket submissions

See: `/portal-design/`

---

Tickets completed:
- 1 Account Locked Out (High)
- 2 No Internet Access (High)
- 3 Network Drive Missing (Medium)
- 4 Printer Not Printing (Medium)
- 5 PC Running Slow (Low)
- 6 Software Install Request (Low)

See: `/ticket-simulations/`

---

## Skills Demonstrated
- Active Directory user and access troubleshooting
- Windows desktop and printer support
- Network connectivity diagnostics
- File share access resolution
- Professional Service Desk communication
- Jira ITSM ticket lifecycle management
