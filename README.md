# Vendor Risk Assessment Lab

A third-party risk assessment (TPRM) of the vendors used by
**Monvive Cloud**, a simulated SaaS booking platform.

This lab remediates finding **F09 ("Vendors never reviewed")**
from my [SOC 2 Readiness Assessment Lab](https://github.com/Wolfofmiami/SOC2-readiness-lab).

## The Result

All three Tier 1 vendors were approved for continued use,
two with conditions.

| Vendor | Residual risk | Decision |
|---|---|---|
| Supabase | HIGH | Approve with conditions |
| Stripe | MEDIUM | Approve with conditions |
| Google Workspace | MEDIUM | Approve |

**Top finding:** Supabase holds the most sensitive customer
data, but its SOC 2 report can't be accessed on the current
plan. It was approved with conditions and a 30-day deadline.

**Key insight:** the biggest risks sat on the customer's side
of shared responsibility, not the vendors'. A vendor's SOC 2
does not cover the customer's own gaps.

## What's Inside

| Step | File | What it is |
|---|---|---|
| 1 | 01-vendor-inventory.csv | 7 vendors tiered by data sensitivity and criticality |
| 2 | 02-due-diligence.md | Trust center review and analysis of Stripe's public SOC 3 |
| 3 | 03-security-questionnaire.md | 16-question questionnaire (SIG Lite / CAIQ structure) |
| 4 | 04-vendor-scorecards.md | Control strength scoring and residual risk |
| 5 | 05-vendor-risk-report.md | Final decisions, conditions, and review schedule |

## Skills Demonstrated

- Vendor inventory and risk tiering
- Vendor due diligence using trust centers and audit reports
- Reading a SOC 3 report: audit period, scope, criteria,
  and carve-out of subservice organizations
- Security questionnaire design (SIG Lite / CAIQ structure)
- Inherent vs residual risk scoring
- Risk-based vendor decisions with conditions and deadlines

## Note

Monvive Cloud is a fictional company created for this lab.
Questionnaire answers come from public vendor documentation.
Items marked "Unknown" would be sent to vendors in a real
assessment.
