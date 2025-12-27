# Printer Not Printing (Medium)

## User report
“Receiving a error when trying to print.”

## Priority
Medium - user impacted but able to continue working without printing.

## Public comment (initial)
Hi, thanks for reporting this. I’m investigating the printer issue now and will update you shortly.

## Internal note
Investigation started. Checking printer status and print queue on affected workstation.

## Troubleshooting (CLIENT01 - GUI)
- Attempted to print from the workstation and was able to reproduce the error
- Checked the printer status and print queue
- Verified the Print Spooler service was stopped and set to Disabled
- Changed Print Spooler startup type to Automati
- Restarted the Print Spooler service
- Cleared the printer spooler cache

## Resolution notes (internal)
Restarted the Print Spooler service via Services.msc

## Public comment (resolution)
I’ve restarted the printer service . Please let me know if printing is now working correctly on your end.

## Closure
Issue resolved and test print completed successfully. Ticket closed.

## Evidence
Add in `evidence/`:
- Ticket overview
- Print queue showing stuck jobs
- services.msc showing Print Spooler restart
- Queue empty
- Ticket closed
