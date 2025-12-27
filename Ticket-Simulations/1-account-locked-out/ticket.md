Account Locked Out (High)

## Environment
- Tool: Jira Service Management (Cloud)
- Lab: lab.local | DC01 | CLIENT01

## User report (Description)
I can’t log in to my computer. It says my account is locked after too many attempts.

## Category / Priority
- Category: Access Management
- Priority: High (user cannot work)

## Public comment (initial response)
Hi John,  
Thanks for reporting this. I’m looking into the login issue now and will update you shortly.

## Internal notes (triage)
Initial triage: user reports account lockout. Checking AD status on DC01.

## Investigation (DC01)
- Opened ADUC (dsa.msc)
- Located user `ablair`
- Confirmed “Account is locked out”

## Resolution
- Unlocked AD account
- Reset password to temporary value
- Enabled “User must change password at next logon”

## Public comment (resolution)
Hi John,  
Your account has been unlocked and your password reset. Please sign in using the temporary password provided and you will be prompted to set a new password.  
Let me know once you’ve confirmed access.

## Verification (CLIENT01)
- Logged into CLIENT01 as `ablair`
- Used temporary password
- Changed password when prompted
- Successful login confirmed

## Closure
- Resolution: Account unlocked and password reset
- Status: Resolved/Closed
- Notes: User confirmed successful login

## Evidence (add screenshots)
Place screenshots in: `evidence/`
Suggested:
1. Ticket created with description + priority
2. Internal note added
3. ADUC showing lockout status
4. ADUC after unlock / reset (or script output if used)
5. Public comment sent
6. Ticket closed
