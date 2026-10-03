# Vendor Risk Scorecards

Prepared by: Jo (assessor)
Date: 2026-10-03
Scope: Tier 1 vendors. Tier 2 vendors get a lighter
annual check and are out of scope for this lab.

## Method

**1. Inherent risk** (from 01-vendor-inventory.csv)
Data sensitivity + business criticality. All Tier 1
vendors start at **High**.

**2. Control strength** (from 03-security-questionnaire.md)

| Answer | Points |
|---|---|
| Yes | 3 |
| Partial | 1 |
| No | 0 |
| Unknown | 0 (unproven = no credit) |

Max score: 16 questions x 3 = 48

| Score | Control strength |
|---|---|
| 75% and up | Strong |
| 50% to 74% | Moderate |
| Below 50% | Weak |

**3. Critical questions:** Q01 (independent audit),
Q02 (report access), Q05 and Q06 (encryption). A "No"
on any critical question raises residual risk one level.

**4. Residual risk matrix**

| Inherent risk | Strong controls | Moderate controls | Weak controls |
|---|---|---|---|
| High | Medium | Medium | High |
| Medium | Low | Medium | Medium |
| Low | Low | Low | Medium |

## Results

| Vendor | Inherent | Score | Control strength | Critical flag? | Residual risk |
|---|---|---|---|---|---|
| Supabase | High | 24 / 48 (50%) | Moderate | YES: Q02 No | **HIGH** |
| Stripe | High | 29 / 48 (60%) | Moderate | No | **MEDIUM** |
| Google Workspace | High | 30 / 48 (63%) | Moderate | No | **MEDIUM** |

## Vendor Notes

### Supabase: HIGH
- Holds our most sensitive data (names, phones, home
  addresses, job photos)
- Score barely reaches Moderate, and 7 of 16 answers
  are Unknown
- Critical flag: we cannot get the SOC 2 report on our
  current plan, so most controls cannot be verified
- Our own side of shared responsibility (row-level
  security) is weak (Lab 1, C06)

### Stripe: MEDIUM
- PCI Level 1 and SOC 2 Type II are strong signals
- Public SOC 3 is 12+ months old; current coverage
  is unverified
- Privacy not covered by audit; subservice
  organizations carved out (fourth-party risk)

### Google Workspace: MEDIUM
- Strongest documentation: no "No" or "Partial" answers
- Score is held down only by Unknowns, which the full
  SOC 2 report would likely resolve
- Expected to move to Strong once the report is reviewed

## Ranking (highest risk first)

1. Supabase: HIGH
2. Stripe: MEDIUM
3. Google Workspace: MEDIUM
