# Vendor Security Questionnaire (Lite)

Prepared by: Jo (assessor)
Date: 2026-10-03
Based on: SIG Lite and CSA CAIQ question structure
Note: Answers come from public documentation reviewed in
02-due-diligence.md. "Unknown" items would be sent to
the vendor to answer directly.

**Answer key:** Yes = proven | Partial = yes with a catch |
No = not done | Unknown = could not verify

## Questions and Answers

| # | Domain | Question | Supabase | Stripe | Google Workspace |
|---|---|---|---|---|---|
| Q01 | Governance | Independent security audit (SOC 2 Type II or ISO 27001) within the last 12 months? | Yes | Partial: public SOC 3 ended Sep 2025 | Yes |
| Q02 | Governance | Will they give us the full SOC 2 report? | No: Team plan or higher only | Yes | Yes |
| Q03 | Access Control | Do their employees need MFA to access customer data? | Unknown | Unknown | Unknown |
| Q04 | Access Control | Can we turn on MFA for our own accounts? | Yes | Yes | Yes |
| Q05 | Data Protection | Is our data encrypted at rest? | Yes: AES-256 | Yes: card numbers never in plain text internally | Yes |
| Q06 | Data Protection | Is our data encrypted in transit? | Yes: TLS | Yes: TLS | Yes: TLS |
| Q07 | Incident Response | Will they notify us of a breach within a set timeframe? | Unknown | Unknown | Unknown |
| Q08 | Incident Response | Is their incident response plan tested every year? | Unknown | Unknown | Unknown |
| Q09 | Business Continuity | Are backups and disaster recovery in place and tested? | Unknown | Yes: availability in SOC 3 scope | Unknown |
| Q10 | Business Continuity | Do they publish a public status page for outages? | Yes | Yes | Yes |
| Q11 | Fourth Parties | Do they review the security of their own vendors? | Unknown | Partial: subservice orgs carved out | Unknown |
| Q12 | Fourth Parties | Do they publish a list of subprocessors? | Yes | Yes | Yes |
| Q13 | Privacy | Will they sign a Data Processing Agreement (DPA)? | Yes | Yes | Yes |
| Q14 | Privacy | Is privacy covered by an independent audit? | Unknown | No: not in SOC 3 | Yes: ISO 27701 |
| Q15 | Vulnerability Mgmt | Do they run a bug bounty or vulnerability disclosure program? | Yes | Yes | Yes |
| Q16 | Vulnerability Mgmt | Do they get independent penetration tests at least yearly? | Unknown | Unknown | Unknown |

## Tally

| Vendor | Yes | Partial | No | Unknown |
|---|---|---|---|---|
| Supabase | 8 | 0 | 1 | 7 |
| Stripe | 9 | 2 | 1 | 4 |
| Google Workspace | 10 | 0 | 0 | 6 |

## Follow-Up Requests (send to vendors)

**All three vendors:**
- Q03: Employee MFA for access to customer data
- Q07: Breach notification timeframe (check the DPA)
- Q08: Annual incident response testing
- Q16: Most recent penetration test summary

**Supabase also:** Q09 backups and DR, Q11 fourth-party
reviews, Q14 privacy audit coverage

**Stripe also:** Q01 current SOC 2 report or bridge letter

**Google also:** Q09 backups and DR, Q11 fourth-party reviews
