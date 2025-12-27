2 – No Internet Access (High)

## User report
“My PC says ‘No internet access’ but others are working.”

## Category / Priority
- Network / Connectivity
- Priority: High

## Public comment (initial)
Hi John,  
Thanks for reporting the issue. I’m investigating the internet connectivity problem on your device now and will update you shortly.

## Internal investigation notes
Checked client network config on CLIENT01.
Verified internal connectivity to DC01.
Confirmed internal resources available but external connectivity failed.

## Troubleshooting steps
1) Internal connectivity (CLIENT01)
- Verified IP in 192.168.100.0/24
- Ping DC01 (192.168.100.10) successful
- DNS resolution for `dc01.lab.local` successful

2) External connectivity (CLIENT01)
- Ping external IP (8.8.8.8) failed
- Web access failed
- Windows showed “No internet access”

3) Root cause
- Internet-facing NAT adapter was disabled
- Host-only adapter remained active

## Resolution
- Re-enabled NAT adapter on CLIENT01
- Verified default gateway restored
- Confirmed external connectivity and web access

## Public comment (resolution)
Hi John,  
I’ve restored internet connectivity on your PC. Please confirm you can access websites as expected.

## Closure
- Resolution: Internet connectivity restored
- Root cause: Disabled internet-facing network adapter
- Status: Resolved/Closed

## Evidence
Add screenshots in `evidence/`:
- Ticket overview
- Ping DC01 success
- External ping fail
- Adapter settings showing NAT disabled
- External ping success after fix
- Closed ticket
