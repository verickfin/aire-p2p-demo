---
type: Concept
title: Vendor Management
description: 'Vendor onboarding, verification at payment time, and master data controls.'
generated:
  by: OKF Wiki Author/1
  at: '2026-10-21T12:20:29.904Z'
---
Vendor management covers the controls applied before a vendor can receive a purchase order and the checks repeated before each payment is released. Its purpose is to ensure the party being paid is the verified legal entity held in master data.

## Vendor Onboarding

New vendors must complete onboarding before any purchase order can be issued:

1. Legal entity verification and tax ID validation
2. Bank account verification (anti-fraud check)
3. Sanctions and compliance screening
4. Master data entry with vendor category and payment terms

The step-by-step version of these requirements is the [Vendor Onboarding Checklist](vendor-onboarding-checklist.md).

## Vendor Verification at Payment Time

Before any payment is released, the system must verify:

- Vendor is active and not suspended
- Bank account matches the master data on file
- Invoice address matches the vendor master record

A mismatch in bank details requires **finance controller review before payment**.

## Related

- Payment terms assigned at master data entry: [Payment Terms](../reference/payment-terms.md) and [Payment Terms Matrix](payment-terms-matrix.md)
- Payment-time checks sit alongside the [Three-Way Match](three-way-match.md) in [Invoice Approval Workflow](../guide/invoice-approval-workflow.md)
