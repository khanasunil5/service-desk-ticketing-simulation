# INC-0004 – Printer Not Printing (Medium)

## User report
“My print jobs are stuck and nothing is printing.”

## Priority
Medium

## Public comment (initial)
Hi, thanks for reporting this. I’m investigating the printer issue now and will update you shortly.

## Internal note
Investigation started. Checking printer status and print queue on affected workstation.

## Troubleshooting (CLIENT01 - GUI)
1) Checked printer status (Printers & scanners)
2) Opened print queue and confirmed jobs stuck
3) Restarted Print Spooler (services.msc)
4) Cleared print queue
5) Test print page successful

## Resolution notes (internal)
Restarted Print Spooler service and cleared stuck print jobs. Printer resumed normal operation.

## Public comment (resolution)
I’ve restarted the printer service and cleared the print queue. Please confirm printing is now working.

## Closure
Resolved/Closed. Test print successful.

## Evidence
Add in `evidence/`:
- Ticket overview
- Print queue showing stuck jobs
- services.msc showing Print Spooler restart
- Queue empty
- Ticket closed
