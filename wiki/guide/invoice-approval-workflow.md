---
type: Guide
title: Invoice Approval Workflow
description: >-
  Step-by-step procedure from invoice receipt through three-way match, variance
  check, approval routing, and payment posting.
generated:
  by: OKF Wiki Author/1
  at: '2026-10-21T12:20:29.904Z'
---
This guide describes the standard path an invoice follows from receipt to payment. It implements the authority levels in [Procurement Policy](../concept/procurement-policy.md) and the match requirement in [Procurement Policy v2](../concept/procurement-policy-v2.md).

## Standard Process

1. **Invoice received** — invoice registered against an open purchase order.
2. **Three-way match** — quantities, unit prices, and totals compared across invoice, PO, and goods receipt ([Three-Way Match](../concept/three-way-match.md)).
3. **Variance check** — variances above 2% or $500 (whichever is lower) are flagged for review.
4. **Approval routing** — routed per the procurement policy thresholds (requesting manager → department head → finance controller + department head → CFO).
5. **Payment posting** — payment scheduled per the vendor's payment terms ([Payment Terms](../reference/payment-terms.md)).

## Exception Handling

- **Price variance** — if the invoice price differs from the PO price, the buyer must confirm the variance is accepted before payment.
- **Quantity mismatch** — short receipts follow the received quantity; over-deliveries require a PO change.
- **Missing goods receipt** — invoices without a goods receipt park in the exception queue for 24h, then auto-reject.

Detailed remediation steps are in [Invoice Exception Handling](../playbook/invoice-exception-handling.md).

## Fraud Prevention

Any request to skip the three-way match or bypass the approval threshold is a red flag. The CFO cannot pre-approve an invoice verbally — all approvals must flow through the system of record with a full audit trail. See [Payables Fraud Controls](payables-fraud-controls.md).
