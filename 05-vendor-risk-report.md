# Vendor Risk Assessment Report: Monvive Cloud

| Prepared by | Jo (Assessor) |
|---|---|
| Date | 2026-10-03 |
| Scope | Tier 1 vendors: Supabase, Stripe, Google Workspace |
| Remediates | Lab 1 finding F09: "Vendors never reviewed" |

## 1. Executive Summary

All three Tier 1 vendors are **approved for continued
use**, two of them **with conditions**.

**Supabase is the highest risk (HIGH).** It holds our
most sensitive customer data, and we cannot access its
SOC 2 report on our current plan. Stripe and Google
Workspace are MEDIUM risk, driven mostly by gaps we
could not verify from public information.

The most important finding: **the biggest risks sit on
our side of shared responsibility**, not the vendors'.
Weak row-level security, incomplete MFA, and unowned
PCI duties are Monvive Cloud problems, and no vendor
audit covers them.

## 2. Approach

1. Built a vendor inventory and tiered 7 vendors by data
   sensitivity and business criticality
2. Reviewed Tier 1 vendors' trust centers and public
   audit reports, including Stripe's SOC 3
3. Answered a 16-question security questionnaire
   (SIG Lite / CAIQ structure) from public evidence
4. Scored control strength and calculated residual risk
5. Made a decision for each vendor

## 3. Results

| Vendor | Residual risk | Decision |
|---|---|---|
| Supabase | HIGH | Approve with conditions |
| Stripe | MEDIUM | Approve with conditions |
| Google Workspace | MEDIUM | Approve |

## 4. Decisions and Conditions

### Supabase: Approve with conditions

| # | Condition | Owner | Due |
|---|---|---|---|
| 1 | Obtain the SOC 2 Type 2 report (upgrade to Team plan or request under NDA) | CTO | 2026-11-02 |
| 2 | Enable row-level security on all tables holding customer data (Lab 1, C06) | CTO | 2026-11-02 |
| 3 | Get answers to 7 Unknown questionnaire items | CTO | 2026-11-02 |
| 4 | Re-assess Supabase after conditions are met | Assessor | 2027-01-01 |

**If conditions are not met:** begin evaluating
alternative database providers with an accessible
SOC 2 Type II report.

### Stripe: Approve with conditions

| # | Condition | Owner | Due |
|---|---|---|---|
| 1 | Obtain the current SOC 2 Type II report or a bridge letter covering Oct 2025 to present | CEO | 2026-11-02 |
| 2 | Review the DPA for breach notification timeframe and privacy terms | CEO | 2026-11-02 |
| 3 | Confirm and complete Monvive Cloud's own PCI compliance requirements | CEO | 2026-12-02 |
| 4 | Ask how Stripe reviews its subservice organizations (fourth-party risk) | CEO | 2026-12-02 |

### Google Workspace: Approve

No conditions on the vendor. Recommended follow-ups:
- Request the SOC 2 report through Compliance Reports
  Manager to resolve Unknown items
- Enforce MFA for every Monvive Cloud user (Lab 1, F05).
  This is OUR control, not Google's.

## 5. Impact on Lab 1 (SOC 2 Readiness)

| Lab 1 item | Before | After |
|---|---|---|
| F09: Vendors never reviewed | Not in place | Partially remediated |
| C15: Vendor reviews before signing and annually | Not in place | Partial: Tier 1 done, Tier 2 pending |

To fully close F09: complete lighter reviews of Tier 2
vendors (Netlify, GitHub, Slack, Angi) and keep the
annual review schedule below.

## 6. Review Schedule

| Vendor | Tier | Next review |
|---|---|---|
| Supabase | 1 | 2027-01-01 (early re-review) |
| Stripe | 1 | 2027-10-03 |
| Google Workspace | 1 | 2027-10-03 |
| Netlify, GitHub, Slack, Angi | 2 | Initial light review by 2026-12-31 |

## 7. Limitations

- Monvive Cloud is a fictional company built for this lab.
- Questionnaire answers come from public documentation,
  not vendor responses. Unknown items would be sent to
  each vendor in a real assessment.
- Full SOC 2 reports were not reviewed. Only Stripe's
  public SOC 3 was read directly.
