# No Internet Access (High)

## User report (Description)
“My PC says ‘No internet access’ but others are working.”

## Category / Priority
- Network / Connectivity
- High

## Public comment (initial)
Hi T Doherty,
Thanks for reporting the issue. I’m investigating the internet connectivity problem on your device now and will update you shortly.

## Internal investigation notes
Checked client network config on CLIENT01.
Verified internal connectivity to DC01.
Confirmed internal resources available but external connectivity failed.

## Investigation
Confirmed the machine has a valid IP address in the internal range and successfully pinged DC01 and resolved the hostname.
Attempted to ping external IPs (8.8.8.8) but there was no response
Windows network status also showed no internet access, at this point it looked like internal access was fine, but outbound traffic wasn’t getting through.

Root cause
The internet-facing (NAT) network adapter on CLIENT01 was disabled.
Only the host-only adapter was active, so the machine could access internal resources but not the internet.

## Resolution
- Re-enabled NAT adapter on CLIENT01
- Verified default gateway restored
- Confirmed external connectivity and web access

## Public comment (resolution)
Hi T Doherty,
I’ve restored internet connectivity on your PC.
Please confirm that you’re now able to access websites as expected

## Closure
Internet connectivity restored after re-enabling the NAT adapter.
User confirmed access was working and the ticket was closed.

## Evidence
Add screenshots in `evidence/`:
- Ticket overview
- Ping DC01 success
- External ping fail
- Adapter settings showing NAT disabled
- External ping success after fix
- Closed ticket
