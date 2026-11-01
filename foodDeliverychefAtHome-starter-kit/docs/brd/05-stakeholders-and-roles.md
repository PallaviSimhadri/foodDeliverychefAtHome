# BRD-FD-001 · Section 5: Stakeholders and roles

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Seven roles use three products, and each role sees only what its job needs.

 Role                  Uses                      Main responsibilities                           Access limits

 Customer              Customer app              Manage profile and addresses, browse,           Own profile, orders, payments,
                                                 order delivery, book chefs, pay, track, rate,   invoices and support history only.
                                                 get help.

 Partner – chef        Partner app (chef         Set availability, view hub shifts and home      Assigned jobs and own profile
                       screens)                  visits, collect kits, travel, cook, update      only. Customer phone masked;
                                                 status, view earnings.                          address shown only during the
                                                                                                 active visit.

 Partner – delivery    Partner app (rider        Go on duty, accept deliveries, navigate,        Assigned deliveries and own
 rider                 screens)                  update pickup and delivery, capture proof.      profile only. Customer phone
                                                                                                 masked; address shown only
                                                                                                 during the active delivery.

 Hub manager           Operations dashboard      Run the local queue, kitchen, dispatch,         Assigned hub or hubs only.
                                                 partner roster and onboarding, kit stock,
                                                 availability and exceptions.

 Customer support      Operations dashboard      Review order context, log issues, apply         Read access to orders. Refunds
 agent                                           approved resolutions, start permitted           above a set limit need approval.
                                                 cancellations and refunds.

 Finance reviewer      Operations dashboard      Reconcile payments, approve refunds             Financial views and approved
                                                 above limit, review settlements and tax         actions only.
                                                 reports.

 Super admin           Operations dashboard      Manage cities, hubs, zones, catalogue,          All hubs. Every sensitive change
                                                 prices, policies, offers, users, partner        is logged.
                                                 approvals and all reports.

Access follows least privilege. Changes to prices, policies, refunds, user roles, partner approvals, stock and service
zones record who changed what and when.
```
