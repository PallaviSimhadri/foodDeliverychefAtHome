# BRD-FD-001 · Section 6: End-to-end service journeys

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Both journeys check serviceability, stock and capacity, then hold what the customer needs before taking payment, so
the customer only pays for what can be delivered.

6.1 Food Order – cooked delivery

1. Customer enters or picks an address. The platform checks it against active service zones.
2. The platform finds eligible hubs: open, offering the service, with stock and rider capacity.
3. Customer browses the hub's available menu and adds dishes. Each dish shows price, serving size, dietary tags and
   allergens.
4. The cart applies the minimum-order rule, delivery fee, offers and taxes, and shows an estimated delivery window.
5. When the customer proceeds to pay, the platform holds the kits for a short time (proposed 10 minutes) and shows
   the time left.
6. Customer pays. The order is confirmed only after the payment gateway verifies the payment.
7. The hub accepts the order, and the kitchen cooks and marks it ready.
8. A rider partner is assigned in the Partner app, picks up and delivers. The customer sees each status change.
9. The rider captures proof of delivery. The customer gets the invoice and can rate or raise an issue.

6.2 Food with Chef – chef at home

1. Customer picks address, dishes, guest count, date and slot.
2. The platform shows only slots where a verified chef, the kits for that date and hub capacity are all free.
3. Customer reviews the itemised price, chef visit fee, taxes, cancellation cut-off and what they must provide at home.
4. When the customer proceeds to pay, the platform holds the kits and the chef's time for a short time.
5. Customer pays. The booking is confirmed, and the customer sees the chef's name, photo and verified status.
6. Before the visit, the hub packs, seals and checks the kits, and the chef confirms collection and starts travel in the
   Partner app.
7. On arrival, the chef shows the sealed kits, and the customer checks them against the order list in the Customer
   app. If they match, the customer shares the visit OTP and the chef enters it in the Partner app, which confirms the
   right chef, the right home and the right kits. The chef then cooks and marks the visit complete.
8. Customer gets the invoice and can rate the food and chef or raise an issue.

6.3 Exception handling

 Exception                             Expected handling                                                        Owner

 Customer does not pay within the      Hold is released and items return to availability. Customer is asked     System
 hold time                             to recheck and try again.

 Payment succeeds after the hold       Items are held again if still free; otherwise a full refund is made      System, then
 expired                               automatically and the customer is told.                                  Finance

 Payment succeeds but the order is     Automatic retry. If it still fails, automatic full refund and customer   System, then
 not created                           notified.                                                                Finance

 No hub, slot, chef, rider or kit      Blocked before payment with a reason. Another slot or service            System
 available                             offered if one exists.

 Dish or kit becomes unusable after    Hub contacts the customer: approved substitute (with consent) or         Hub manager
 confirmation (spoiled or damaged)     partial or full refund.

 Chef or rider declines, is delayed    Reassign. Notify the customer with a new time. If no one is              Hub manager
 or cannot attend                      available, cancel and refund in full.

 Chef arrives late beyond the          Customer may cancel for a full refund or accept a stated                 Hub manager,
 allowed limit                         compensation.                                                            Support

 Incomplete address or wrong           Partner reports it in the Partner app. Hub calls the customer. The       Partner, Hub
 phone number                          no-show timer starts.

 Customer unreachable or not           No-show policy applies: wait time, contact attempts, then cancel         Hub manager
 home                                  with the agreed charge.

 Home facilities not usable (no gas,   Chef reports with a photo. Hub decides: cook a reduced menu,             Chef, Hub manager
 no stove)                             cook at the hub and deliver, or cancel per policy.

 Missing, wrong or damaged items       Customer raises it within the allowed time with a photo. Support         Support
                                       resolves per refund policy.

 Refund pending, failed or needs       Tracked in the refund queue. Escalated if it passes the refund time      Finance
 review                                limit.

 Safety incident during a visit or     Partner or customer uses SOS. Hub and the client's safety contact        Hub manager, Client
 delivery                              are alerted at once.                                                     safety owner

 Kits at arrival are missing, wrong    Customer reports it in the Customer app instead of sharing the           Chef, Hub manager
 or damaged                            visit OTP, and the chef reports it in the Partner app. The hub sends
                                       replacement kits, agrees a reduced menu with a partial refund, or
                                       cancels with a full refund.
```
