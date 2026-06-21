# Offboarding Checklist

Run this checklist whenever a person (including Brian) departs or loses access to CCG Labs systems. Designed for a solo operator context where "offboarding" may mean emergency recovery or transitioning to a successor.

## GitHub

- [ ] Remove from **CCG-Labs** org (`https://github.com/orgs/CCG-Labs/people`)
- [ ] Revoke any **PATs** they created (`https://github.com/organizations/CCG-Labs/settings/personal-access-tokens`)
- [ ] Remove any **deploy keys** they added across repos
- [ ] Reassign or update **CODEOWNERS** entries that reference their GitHub handle — point to a team or a successor
- [ ] Transfer any **repos or GitHub Apps** owned under their personal account into the CCG-Labs org
- [ ] If they were an Owner, verify at least one other Owner remains; if not, promote the break-glass account (`ccglabsbreakglass`) before removing

## AWS

- [ ] Delete their **IAM user** or **SSO assignment** in the management account (773629544325)
- [ ] Audit **OIDC trust policies** — check if any role's trust policy is scoped to a personal fork or branch they controlled
- [ ] Rotate any **secrets** they had access to (SES, Lambda env vars, etc.)

## Domains & DNS (Namecheap / Route 53)

- [ ] Change **Namecheap account password** if they had credentials
- [ ] Audit **Route 53 hosted zones** for any records they may have managed

## Communication & Accounts

- [ ] Revoke access to **email** (brian.reich@thecoresolution.com or client aliases)
- [ ] Remove from any **Slack / messaging** workspaces
- [ ] Update **client contact records** in `CCG Labs Agent/Clients/` to reflect the new point of contact

## Documentation

- [ ] Update `CCG Labs Agent/Subagents/` if any agent definitions referenced their name or credentials
- [ ] Note the departure and effective date in `CCG Labs Agent/Daily/<YYYY-MM-DD>.md`

## Break-Glass Account (ccglabsbreakglass)

If Brian is the one departing and a successor is taking over:
- [ ] Transfer `ccglabsbreakglass` credentials (stored in password manager) to the successor
- [ ] Rotate the break-glass account password and 2FA after transfer
- [ ] Confirm the successor can access org Settings before Brian's account is removed
