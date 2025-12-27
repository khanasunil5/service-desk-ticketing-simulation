# 3 – Network Drive Missing (Medium)

## Scenario
- User: j.smith
- Machine: CLIENT01
- Drive: Finance → \\DC01\Finance
- Required group: GG_Share_Finance_RW

## User report
“Hi, I can’t see the Finance drive on my computer. It was there before but has disappeared.”

## Priority
Medium (user can work but missing access)

## Public comment (initial)
Hi John, thanks for reporting this.  
I’m checking your access to the Finance drive now and will update you shortly.

## Investigation (DC01)
- Checked ADUC → j.smith → Member Of
- GG_Share_Finance_RW not present
- Confirmed correct group exists: GG_Share_Finance_RW

## Internal note
Checked AD user properties — user is not a member of the Finance share access group. Correct group identified: GG_Share_Finance_RW.

## Resolution
- Added user j.smith to GG_Share_Finance_RW
- On CLIENT01, remapped drive:
  - F: → \\DC01\Finance
  - Reconnect at sign-in enabled
- Verified read/write:
  - Created testfile.txt successfully

## Closure notes
Root cause: missing AD group membership.
Fix: added correct group + remapped drive + verified access.

## Evidence
Screenshots to add in `evidence/`:
- User “Member Of” tab (missing group)
- Group properties (GG_Share_Finance_RW)
- Drive mapping screen or Explorer showing F:
- testfile.txt created successfully
- Closed ticket view
