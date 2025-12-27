# Service Desk Ticketing Simulation (Jira ITSM)

## Overview
This project demonstrates entry-level IT Support / Service Desk skills using:
- Jira Service Management (Cloud)
- A Windows Active Directory home lab

Focus: ticket handling, troubleshooting, and user communication.

---

## Lab Architecture
**Domain:** lab.local  
**Network:** Host-only (isolated internal network)

**Domain Controller (DC01)**
- Windows Server 2019
- IP: 192.168.100.10 (static)
- Services: AD DS, DNS, Event Viewer

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

## Ticket Simulations
Each ticket includes:
- User-submitted request
- Agent triage (internal notes)
- Troubleshooting steps
- Resolution and verification
- Evidence screenshots

Tickets completed:
- INC-0001 Account Locked Out (High)
- INC-0002 No Internet Access (High)
- INC-0003 Network Drive Missing (Medium)
- INC-0004 Printer Not Printing (Medium)
- INC-0005 PC Running Slow (Low)
- INC-0006 Software Install Request (Low)

See: `/ticket-simulations/`

---

## Skills Demonstrated
- Active Directory user and access troubleshooting
- Windows desktop and printer support
- Network connectivity diagnostics
- File share access resolution
- Professional Service Desk communication
- Jira ITSM ticket lifecycle management
