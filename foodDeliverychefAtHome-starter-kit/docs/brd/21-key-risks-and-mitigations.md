# BRD-FD-001 · Section 21: Key risks and mitigations

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The two risks most likely to hurt launch are the size of the full launch scope and a safety incident during a home visit.

 Risk                       Impact                                  Mitigation                                      Owner

 Full scope at launch       Two mobile apps, a dashboard            Milestone gates, change control, early          Client, Delivery
                            and shared services at once             decisions on OD-01 to OD-08, and a pilot        lead
                            stretch delivery time and testing.      before public launch.

 Safety incident during a   Harm to a customer or partner;          Verified partners only, visit OTP, SOS,         Client safety
 home visit or delivery     serious damage to the brand.            masked numbers, incident owner (Section         owner
                                                                    11).

 Partner app serving two    A partner sees the wrong jobs,          Screens and permissions by approved role,       Delivery lead
 roles                      or the app becomes cluttered.           tested separately for each role (UAT-14).

 Partner adoption           Partners on low-end phones or           Agreed minimum phone, offline-tolerant          Operations
                            weak networks struggle to use           status updates, local languages, short
                            the app.                                training at onboarding.

 Food safety in transit     Kits spoil on the way to a home         Pack-time limit, insulated bags, handover       Food operations
                            visit.                                  record, expiry checks.

 Wrong or stale stock       Orders confirmed that cannot be         Holds before payment, stock history, daily      Hub manager
                            fulfilled; refunds and bad ratings.     kit plans, low-stock alerts, regular counts.

 Overbooked chefs or        Late arrivals and cancellations.        Slots that account for visit length, travel     Operations
 slots                                                              and shifts; chef time held before payment;
                                                                    reassignment flow.

 Unclear cancellation       Disputes, inconsistent refunds          Approved policy matrix shown before             Client, Finance
 policy                     and revenue loss.                       payment; audit of exceptions.

 Overlapping hub zones      Confusing hub choice, prices or         One fixed hub-selection rule, tested at         Operations
                            ETAs.                                   boundaries.

 Third-party outage         OTP, payments, maps or                  Retries, clear customer messages, manual        Delivery lead, Ops
                            messages fail.                          fallback and vendor escalation.

 Poor menu data at launch   Wrong prices, portions or               Signed catalogue template; nothing              Menu owner
                            allergens reach customers.              published without menu owner approval.

 App store review delays    Launch date slips for one or            Early test submissions, client-owned            Delivery lead
                            both apps.                              accounts set up in M2, clear permission
                                                                    wording.

 Unknown peak volumes       Slow or unstable app at meal            Volume forecasts (OD-17) and load testing       Client, Delivery
                            times.                                  before launch.                                  lead

 Unclear ownership after    Incidents, renewals or store            Named account owners, support hours and         Client
 launch                     issues go unhandled.                    escalation agreed before go-live (OD-19,
                                                                    OD-20).
```
