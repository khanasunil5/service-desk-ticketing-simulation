# Account Locked Out (High)

## Environment
Ticketing Platform: Jira Service Management (Cloud) with a Lab Environment: Windows Active Directory domain lab.local (DC01, CLIENT01)

## User report (Description)
I can’t log in to my computer. It says my account is locked after too many attempts.

## Category / Priority
- Access Management
- High - user cannot work

## Public comment (initial response)
Hi,  
Thanks for reporting this. I’m looking into the login issue now and will update you shortly.

## Internal notes (triage)
Initial triage: user reports account lockout. Checking AD status on DC01.

## Investigation (DC01)
-Checked user account `ablair` in Active Directory on DC01.  
Account confirmed locked due to multiple failed login attempts.

## Resolution
Unlocked the user account in Active Directory and reset the password to a temporary value.  
Set the account to require a password change at next logon.

## Public comment (resolution)
Hi,  
Your account has been unlocked and your password reset. Please sign in using the temporary password provided and you will be prompted to set a new password.  
Let me know once you’ve confirmed access.

## Verification (CLIENT01)
User logged in successfully on CLIENT01 and changed password as prompted.

## Closure
Issue resolved. User confirmed access restored.  
Ticket closed.

## Evidence (add screenshots)
Screenshots saved in the `evidence/` folder :
1. Ticket created with description + priority
2. Internal note added
3. ADUC showing lockout status
4. ADUC after unlock / reset (or script output if used)
5. Public comment sent
6. Ticket closed
