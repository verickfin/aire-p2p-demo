---
type: Playbook
title: Invoice Exception Handling
description: >-
  How to resolve price variances, quantity mismatches, and missing goods
  receipts so a flagged invoice can be approved or rejected.
generated:
  by: OKF Wiki Author/1
  at: '2026-10-21T12:20:29.904Z'
---
Use this playbook when an invoice fails the variance check in [Invoice Approval Workflow](../guide/invoice-approval-workflow.md) — that is, when a variance exceeds 2% or $500, whichever is lower. The goal is to clear the exception with an auditable decision, never to release payment outside the match.

## Price Variance

1. Compare the invoiced unit price against the PO price.
2. Route to the buyer, who must confirm the variance is accepted **before** payment.
3. If the buyer does not accept, hold the invoice; do not proceed to approval routing.

## Quantity Mismatch

1. **Short receipt** — pay against the received quantity, not the invoiced quantity.
2. **Over-delivery** — a PO change is required before the excess can be accepted and paid.

## Missing Goods Receipt

1. The invoice parks in the exception queue.
2. After 24 hours without a goods receipt, the invoice **auto-rejects**.
3. To recover, obtain the goods receipt and re-register the invoice against the open PO.

## Escalation and Boundaries

- Approval of the cleared invoice still follows the value thresholds in [Procurement Policy](../concept/procurement-policy.md); an exception never lowers the required approver.
- The [three-way match](../concept/three-way-match.md) is mandatory for all payments regardless of amount, and verbal pre-approval never substitutes for it — treat such a request per [Payables Fraud Controls](payables-fraud-controls.md).
- Where the exception involves vendor bank or address data, apply the payment-time checks in [Vendor Management](../concept/vendor-management.md).
