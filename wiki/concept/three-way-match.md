---
type: Concept
title: Three-Way Match
description: >-
  The mandatory comparison of invoice, purchase order, and goods receipt that
  must clear before any payment is released.
generated:
  by: OKF Wiki Author/1
  at: '2026-10-21T12:20:29.904Z'
---
The three-way match compares quantities, unit prices, and totals across three documents — the invoice, the purchase order, and the goods receipt — before a payment is scheduled. It is mandatory for **all** payments regardless of amount, under both [Procurement Policy](procurement-policy.md) and [Procurement Policy v2](procurement-policy-v2.md).

## What Is Compared

- Quantities invoiced vs ordered vs received
- Unit prices invoiced vs ordered
- Invoice total vs PO total

## Non-Negotiables

- Verbal pre-approval is never a reason to skip the match; all approvals must flow through the system of record with a full audit trail.
- Invoices with no goods receipt park in the exception queue for 24 hours and then auto-reject.
- Variances above 2% or $500 (whichever is lower) are flagged for review before approval routing.

## Related

- Match execution and routing: [Invoice Approval Workflow](../guide/invoice-approval-workflow.md)
- Handling flagged matches: [Invoice Exception Handling](../playbook/invoice-exception-handling.md)
- Attempts to bypass the match are treated as fraud indicators: [Payables Fraud Controls](payables-fraud-controls.md)
