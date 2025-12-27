# Network Drive Missing (Medium)

User report
“Hi, I can’t see the Finance drive on my computer. It was there before but has disappeared.”

### Priority
Medium (user can work but missing access)

## Public comment (initial)
Hi T Doherty, thanks for reporting this.  
I’m checking your access to the Finance drive now and will update you shortly.

## Investigation (DC01)
Checked the user account in Active Directory to confirm access to the Finance share.
Reviewed group membership for j.smith and found the required Finance access group was not assigned.
Verified that the correct security group (Finance_Uesrs) exists and is used for access to the Finance share.

## Internal note
Checked AD user properties — user is not a member of the Finance share access group. Correct group identified: Finance_users.

## Resolution
Added T Doherty to the Finance access group in Active Directory.
On the user’s workstation, remapped the Finance drive to \DC01\Finance and set it to reconnect at sign-in.
Tested access by creating a file in the share to confirm read/write permissions.

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
