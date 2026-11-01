# BRD-FD-001 · Section 8: Functional requirements

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Each requirement has an ID used in testing (Section 18). Priority: Must = needed at launch; Should = strongly
preferred at launch; Later = after launch. The client confirms final priorities.

8.1 Customer app (FR-CUS-001 to FR-CUS-018)

FR-CUS-001 — Sign up and sign in with mobile number and OTP. Sessions expire securely; customer can log out.                                          Must

FR-CUS-002 — Manage profile, saved addresses with map pin, delivery instructions and location permission.                                             Must

FR-CUS-003 — Check serviceability by address and show clearly which services are available there.                                                     Must

FR-CUS-004 — Choose Food Order or Food with Chef, each with its own menu, fees and rules.                                                             Must

FR-CUS-005 — Browse, search and filter dishes with photo, description, price, serving size, dietary tags and allergens.                               Must

FR-CUS-006 — Show availability by hub, service, time and stock. Unavailable dishes cannot be added.                                                   Must

FR-CUS-007 — Cart with quantities and an itemised price summary.                                                                                      Must

FR-CUS-008 — Enforce minimum-order and guest-count rules and explain any failure in plain words.                                                      Must

FR-CUS-009 — For chef visits, pick date, slot, guest count and notes such as kitchen access or dietary needs.                                         Must

FR-CUS-010 — Show delivery fee, chef visit fee, taxes, discounts and total before payment.                                                            Must

FR-CUS-011 — Pay by UPI, cards, net banking and wallets through the payment gateway, and see the payment result.                                      Must

FR-CUS-012 — See confirmation, order details, cancellation eligibility and status history.                                                            Must

FR-CUS-013 — Track the rider for deliveries. For chef visits, see the chef's name, photo, verified status and arrival ETA.                            Must

FR-CUS-014 — See the visit OTP and the list of ordered kits on the visit day. On arrival, check the chef's kits against                               Must
the list, then share the OTP to confirm, or report a missing, wrong or damaged kit instead.

FR-CUS-015 — Use an in-app SOS during a chef visit that alerts the hub and the client's safety contact, with one-tap                                  Must
call to 112.

FR-CUS-016 — Download a tax invoice for each completed order or booking.                                                                              Must

FR-CUS-017 — Request cancellation or help, see eligibility and the expected refund amount and time.                                                   Must

FR-CUS-018 — Receive order notifications by push, SMS or WhatsApp, with consent recorded.                                                             Must

8.1 Customer app (continued: FR-CUS-019 to FR-CUS-026)

FR-CUS-019 — Delete account and personal data on request, except records the law requires the client to keep.                       Must

FR-CUS-020 — See the time left to complete payment while items are held; if it runs out, availability is rechecked.                 Must

FR-CUS-021 — View order history and reorder, with current prices and availability rechecked.                                     Should

FR-CUS-022 — Rate and review food, chef and delivery after completion, subject to moderation.                                    Should

FR-CUS-023 — Access FAQs, support contacts and a reference number for each reported issue.                                       Should

FR-CUS-024 — Pre-order a Food Order for later the same day or the next day.                                                      Should

FR-CUS-025 — Use the app in the launch languages agreed with the client.                                                         Should

FR-CUS-026 — Save favourite dishes and get dish recommendations.                                                                    Later

8.2 Partner app

One app serves chefs and delivery riders. A hub manager registers each partner, a super admin approves their role
after verification, and the app then shows only that role's screens. If the client uses a third-party delivery company
instead of in-house riders, the rider screens are replaced by that company's integration (Section 16).

8.2.1 All partners

 ID                   Requirement                                                                                        Priority

 FR-PTR-001           Sign in with OTP on the mobile number registered by the hub. Only approved partners can             Must
                      sign in.

 FR-PTR-002           Show only the screens for the partner's approved role: chef, rider, or both if the client allows    Must
                      it (OD-24).

 FR-PTR-003           Show profile with photo, role, home hub and verification status. Partners cannot change             Must
                      their own role or verification.

 FR-PTR-004           Go on or off duty, and view shifts set by the hub.                                                  Must

 FR-PTR-005           Receive new-job alerts with sound and vibration, and see all assigned jobs in one list.             Must

 FR-PTR-006           Report an issue on any job (delay, customer unreachable, address problem, damaged items,            Must
                      safety concern), with a photo.

 FR-PTR-007           Use an SOS button during any active job that alerts the hub and the client's safety contact,        Must
                      with one-tap call to 112.

 FR-PTR-008           Share location only while on an active job, and stop when the job ends.                             Must

 FR-PTR-009           Open navigation to the hub or customer, and call the customer through a masked number.              Should

 FR-PTR-010           View job history and earnings per the agreed pay model (viewing only; payouts are out of            Should
                      scope).

 FR-PTR-011           Keep working on weak networks: status updates are saved on the phone and sent when the              Should
                      connection returns.

 FR-PTR-012           Use the app in the launch languages agreed with the client.                                         Should

8.2.2 Chef screens

FR-CHF-001 — See hub kitchen shifts and home visits in one schedule.                                                              Must

FR-CHF-002 — View each visit: dishes, guest count, kit checklist, address, timing, customer notes and home checklist.             Must

FR-CHF-003 — Accept or decline a visit if the client turns this on; otherwise visits are assigned by the hub.                     Must

FR-CHF-004 — Tick off the kit checklist at collection. Any missing kit alerts the hub before the chef leaves.                     Must

FR-CHF-005 — Update status: kits collected, en route, arrived, cooking, completed.                                                Must

FR-CHF-006 — On arrival, show the customer the sealed kits against the order, then start the visit only after entering            Must
the customer's visit OTP.

FR-CHF-007 — Report unusable home facilities with a photo, so the hub can decide what to do.                                      Must

FR-CHF-008 — Confirm the client's hygiene checklist at the start and end of each visit.                                        Should

8.2.3 Rider screens

FR-RID-001 — Receive delivery assignments while on duty, and accept them.                                                         Must

FR-RID-002 — View pickup hub, customer address, delivery instructions, order reference and promised window.                       Must

FR-RID-003 — Update status: at hub, picked up, en route, at customer, delivered.                                                  Must

FR-RID-004 — Capture proof of delivery by customer OTP or photo, as the client decides.                                           Must

FR-RID-005 — Report a failed delivery with a reason, and return the order to the hub.                                             Must

8.3 Operations dashboard: hub manager screens

 ID                   Requirement                                                                                      Priority

 FR-HUB-001           View live queues of orders and bookings, filtered by status, service, promised time and           Must
                      priority.

 FR-HUB-002           Accept, reject or flag orders by capacity and policy, with a recorded reason.                     Must

 FR-HUB-003           Kitchen queue showing dishes, kits, preparation target time and ready status.                     Must

 FR-HUB-004           Assign or swap chefs for hub cooking and home visits, blocking double-booking across              Must
                      shifts, travel and visit length.

 FR-HUB-005           Assign riders, or send jobs to the delivery company, and monitor pickup and dispatch.             Must

 FR-HUB-006           Pack, seal and verify kits for each home visit against the booking checklist before handover      Must
                      to the chef.

 FR-HUB-007           Track kit stock: on hand, held, allocated by date, low-stock alerts, batch and expiry where       Must
                      used, adjustments and counts.

 FR-HUB-008           Mark a dish or kit unavailable so new orders that cannot be fulfilled are blocked.                Must

 FR-HUB-009           Manage partner rosters, shifts and hub closures.                                                  Must

 FR-HUB-010           Register new partners for the hub (mobile number, role, documents) and send them for              Must
                      approval.

 FR-HUB-011           Handle exceptions with notes, reasons, actions taken and escalation status.                       Must

 FR-HUB-012           Receive SOS alerts from active visits and deliveries, with partner and customer details, and      Must
                      acknowledge them.

 FR-HUB-013           View hub reports: sales, order status, cancellations, fulfilment times, stock and partner use.    Should

8.4 Operations dashboard: super-admin screens

 ID                   Requirement                                                                                     Priority

 FR-ADM-001           Create, edit, pause and reopen cities and hubs, with address, hours and supported services.      Must

 FR-ADM-002           Set each hub's service zone as a radius, drawn map area or postal codes, and handle              Must
                      overlaps.

 FR-ADM-003           Manage the catalogue: dishes, serving sizes, kit mappings, recipes, photos, dietary labels       Must
                      and allergens.

 FR-ADM-004           Set prices, fees, offers and time limits at platform, city or hub level (Section 4.3).           Must

 FR-ADM-005           Manage customers, partners, hub managers, support agents, finance reviewers and their            Must
                      roles.

 FR-ADM-006           Approve a partner's role only after verification is recorded; suspend or deactivate a partner    Must
                      with immediate effect.

 FR-ADM-007           Set minimum order, guest rules, booking notice, slot length, maximum bookings, hold time         Must
                      and cancellation cut-offs.

 FR-ADM-008           Store each hub's food licence number and the invoicing details for each city or state.           Must

 FR-ADM-009           Review payments, refunds, settlements and reconciliation.                                        Must

 FR-ADM-010           View consolidated and hub-wise sales, orders, discounts, taxes, refunds, ratings and             Must
                      performance.

 FR-ADM-011           Keep an audit trail of every sensitive change and admin action.                                  Must

 FR-ADM-012           Pause a hub or a whole area temporarily without deleting history.                                Must

 FR-ADM-013           Turn optional features on or off by city or hub (WhatsApp, masked calling, chef accept or        Should
                      decline).

 FR-ADM-014           Edit banners, promotions, notification templates and customer-facing policy text.                Should

 FR-ADM-015           Export permitted reports to Excel or CSV.                                                        Should

8.5 Orders, holds, payments, invoices and support

FR-OPS-001 — Give each order or booking one reference number and a timestamped status history.                                   Must

FR-OPS-002 — Turn held kits into confirmed reservations on payment, use them on cooking or packing, and release                  Must
them on valid cancellation.

FR-OPS-003 — Prevent duplicate orders and charges when customers retry or the gateway repeats a message.                         Must

FR-OPS-004 — Track payment and refund status separately from order and booking status.                                           Must

FR-OPS-005 — Allow full or partial refunds only as the approved policy and gateway permit.                                       Must

FR-OPS-006 — Generate a tax invoice for each completed order or booking, from the correct city or state entity, using            Must
the prices fixed at confirmation.

FR-OPS-007 — Send notifications on every event listed in Section 10.                                                             Must

FR-OPS-008 — Keep completed, cancelled and refunded records for reporting, support and legal retention.                          Must

FR-OPS-009 — Hold kits and, for chef visits, the chef's time when the customer proceeds to pay, and release them                 Must
automatically when the hold expires.

FR-OPS-010 — Check payments against the gateway automatically, and refund in full any paid order that cannot be                  Must
fulfilled.

FR-OPS-011 — Create support cases linked to orders, with category, priority, owner, notes, resolution and time                Should
stamps.
```
