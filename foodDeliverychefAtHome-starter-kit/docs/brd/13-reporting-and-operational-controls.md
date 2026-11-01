# BRD-FD-001 · Section 13: Reporting and operational controls

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Reports give each role the numbers it acts on, filtered by date, city, hub and service.

13.1 Standard reports

Sales and orders: Volume and value by date, city, hub, service, dish and status.                            Super admin, Hub mgr

Revenue breakdown: Gross value, discounts, delivery and chef fees, taxes, refunds and net collection.                        Finance

Payments and refunds: Success and failure rates, expired holds, late-payment refunds, pending and failed refunds,            Finance
reconciliation differences.

Kitchen performance: Order-to-accept, accept-to-ready, ready-to-pickup and delivery times.                           Hub manager

Chef visit performance: Booking lead time, on-time arrival, visit length, reassignments, cancellations.              Hub manager

Inventory: On hand, held, allocated by date, used, low stock, expiry, wastage and adjustments.                       Hub manager

Customer experience: Ratings, complaints, cancellation reasons, refunds and repeat orders.                   Super admin, Support

Partner activity: Jobs, hours on duty, on-time rate and ratings per chef and rider, by hub and shift.                Hub manager

Safety incidents: Incidents by type, hub, status, acknowledgement time and outcome.                            Client safety owner

13.2 Controls

   Every report shows its date range, time zone, filters and last refresh time.
   Financial totals reconcile to transaction records and to the payment gateway's reports.
   Exports are role-based. Customer personal data appears only where the role needs it.
   High-risk actions need a second approval above client-set limits: large refunds, manual price edits and large stock
   adjustments.
```
