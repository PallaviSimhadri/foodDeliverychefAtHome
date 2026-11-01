# BRD-FD-001 · Section 4: Business model and scope

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Both services share one catalogue, one kit inventory and one hub network; they differ only in where the food is cooked
and who carries it.

4.1 Service lines

   Food Order – cooked delivery: Customer experience: Customer picks dishes, pays and receives freshly cooked
   food at the chosen address. Fulfilment path: Eligible hub holds the kits, cooks them, and a rider partner collects
   and delivers.
   Food with Chef – chef at home: Customer experience: Customer picks dishes, guest count, date and slot. A chef
   arrives with the kits and cooks at home. Fulfilment path: Hub holds kits and a verified chef's time, packs and
   checks the kits, and the chef partner travels, cooks and completes the visit.

4.2 Hub operating model

   Each hub has a unique ID, address, operating hours, service zone, supported services, menu availability, kit stock,
   partner roster and capacity.
   Authorised admins create, edit, pause and close hubs. Past orders stay linked to the hub that fulfilled them.
   A hub can pause new orders, close one service, mark a dish unavailable or block a slot without affecting other
   hubs.
   Partners belong to a home hub and can be moved or shared between hubs by an admin.
   If no hub can serve an address or slot, the customer is told before payment. The platform never assigns a hub that
   cannot serve the order.

4.3 Configuration levels

Settings are layered so a new city or hub inherits sensible defaults and only overrides what differs.

 Setting                                      Platform default         City override                 Hub override

 Menu and dishes                              Master catalogue         Dishes offered in that city   Dishes available at that
                                                                                                     hub

 Prices                                       Base price               City price                    Hub price, if approved

 Minimum-order rule                           Default rule             Yes                           Yes

 Delivery and chef visit fees                 Default fees             Yes                           Yes

 Taxes and invoicing entity                   Default                  Yes (state registration)      No

 Operating hours                              –                        –                             Yes

 Service zone                                 –                        –                             Yes

 Booking notice, slot length, buffers         Default rule             Yes                           Yes

 Checkout hold time                           Default                  No                            No

 Cancellation policy                          Default policy           Yes                           No

 Offers and promotions                        Platform-wide            City-only                     Hub-only

 Optional features (WhatsApp, masked          On or off                Yes                           Yes
 calling, chef accept/decline)

 Support contacts and languages               Default                  Yes                           No

4.4 In-scope deliverables

1. Customer app for Android and iOS.
2. Partner app for Android and iOS: one app for chefs and delivery riders, showing each partner only the screens for
   their approved role.
3. Operations dashboard (web) for hub managers, support agents, finance reviewers and super admins, with screens
   by role.
4. Shared services: users and roles, partner onboarding, catalogue, serviceability, orders and bookings, holds, kit
   inventory, scheduling, dispatch, payments, refunds, invoices, notifications, support cases and reporting.
5. Launch support: testing, production setup, store submission for both apps, a pilot at one hub, documentation and
   handover.
```
