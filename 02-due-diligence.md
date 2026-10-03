# Vendor Due Diligence: Tier 1 Vendors

Performed by: Jo (assessor)
Date: 2026-10-03
Method: Review of public trust centers, security pages,
and published audit reports.

## V01: Supabase (Customer database)

| Item | Finding |
|---|---|
| Trust center | security.supabase.com |
| Certifications | SOC 2 Type 2, ISO 27001, HIPAA |
| SOC 2 report available? | Only on Team plan or higher. NOT obtainable on our current plan |
| Encryption | AES-256 at rest, TLS in transit |
| Shared responsibility | Supabase secures infrastructure. WE secure row-level security, API keys, and access |

**Concerns:**
- Cannot review the full SOC 2 report without upgrading
- Our row-level security is only partial (Lab 1, C06),
  so our side of shared responsibility is weak

## V02: Stripe (Payment processing)

| Item | Finding |
|---|---|
| Trust center | docs.stripe.com/security |
| Certifications | PCI DSS Level 1 Service Provider; SOC 1 and SOC 2 Type II |
| SOC 2 report available? | Yes, upon request and from the dashboard |
| Public report | SOC 3 (reviewed) |
| SOC 3 audit period | Oct 1, 2024 to Sep 30, 2025 (over 12 months old) |
| SOC 3 system in scope | Global payment, revenue and finance automation |
| SOC 3 criteria covered | Security, availability, confidentiality (not processing integrity or privacy) |
| Subservice organizations | Yes. Carve-out method: their controls are NOT tested in this report |

**Concerns:**
- Stripe being PCI compliant does NOT make us PCI
  compliant. We still have our own PCI obligations.
- Most recent public SOC 3 ended Sep 30, 2025. Coverage
  gap of 12+ months. Request current report or bridge letter.
- Privacy criteria not covered in the SOC 3. Customer
  personal data handling should be reviewed through
  Stripe's DPA and privacy policy instead.
- Subservice organizations are carved out. Fourth-party
  risk is unverified. Ask Stripe how they review their
  own vendors.

## V03: Google Workspace (Email and documents)

| Item | Finding |
|---|---|
| Trust center | Google Cloud Compliance Resource Center |
| Certifications | ISO 27001, 27017, 27018, 27701; SOC 2; SOC 3 |
| SOC 2 report available? | Yes, via Compliance Reports Manager |
| Bridge letters | Yes, issued to cover gaps since the last report |

**Concerns:**
- Strongest documentation of the three. Main risk is
  on OUR side: MFA not verified for all users
  (Lab 1, F05)

## Summary

| Vendor | Independent audit? | Report obtained? | Biggest concern |
|---|---|---|---|
| Supabase | Yes | No (plan limit) | Can't verify report; our RLS is weak |
| Stripe | Yes | Public SOC 3 only | Report 12+ months old; fourth-party risk carved out |
| Google Workspace | Yes | Available on request | Our MFA coverage |

## Key Takeaway

All three vendors have independent audits and strong
security programs. The biggest risks sit on Monvive
Cloud's side of shared responsibility: weak row-level
security, incomplete MFA, and unmet PCI duties. A
vendor's SOC 2 does not cover the customer's own gaps.
