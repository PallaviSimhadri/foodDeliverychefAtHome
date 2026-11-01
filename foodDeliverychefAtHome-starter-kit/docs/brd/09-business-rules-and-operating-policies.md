# BRD-FD-001 · Section 9: Business rules and operating policies

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Every rule below is configurable; the client must confirm the open ones before build starts on that area.

 ID & Rule Name              Rule Definition                                                         Status

 BR-001 Hub selection        Choose a hub that serves the address, offers the service, is open,      Client to choose tie-breaker
                             has the kits and has capacity. If several qualify, use the client's
                             tie-breaker (for example nearest, fastest or least busy).

 BR-002 Minimum order        Configurable by guest count and basket value. Discussed so far:         Open (OD-01)
                             2 people or ₹1,200. The exact rule (either, both, or whichever is
                             higher) and whether it differs by service must be confirmed.

 BR-003 Service zones        A hub never accepts an order outside its zone. Behaviour at             Open (OD-07)
                             overlapping zones and boundaries must be agreed.

 BR-004 Kit availability     Confirm only when all kits can be held. Substitutions need              Proposed
                             customer consent. No silent substitution.

 BR-005 Hold before          When the customer proceeds to pay, the kits and any chef time           Open on hold time (OD-23)
 payment                     are held for a short time (proposed 10 minutes). Unpaid holds
                             are released automatically. A payment that arrives late is either
                             re-held or refunded in full.

 BR-006 Price                Show all prices, fees, discounts and taxes before payment.              Proposed
 transparency

 BR-007 Price snapshot       Prices, fees and taxes are fixed when the order is confirmed.           Proposed
                             Later menu or price changes never change a confirmed order or
                             its invoice.

 BR-008 Chef slots           A slot is bookable only if booking notice, a verified chef's            Open config (OD-04)
                             availability, visit length, travel buffer, kits for that date and hub
                             hours all fit.

 BR-009 Visit length         Each booking has a planned duration based on dishes and guest           Open (OD-03)
                             count. Overtime rules and charges must be agreed.

 BR-010 Cancellation         Separate rules for Food Order and Food with Chef, by stage. Cut-        Open (OD-05)
                             off, fee and refund shown before payment.

 BR-011 No-show              Set wait time and contact attempts before a partner marks a no-         Open (OD-05)
                             show, and the charge that applies.

 BR-012 Reassignment         If a chef or rider becomes unavailable, operations can reassign,        Proposed
                             notify the customer, or cancel and refund.

 BR-013 Proof of             Delivery needs OTP or photo proof. A chef visit needs the visit         Open on proof & OTP (OD-22)
 completion                  OTP at arrival, which also records the customer's confirmation of
                             the kits, and a completion time stamp.

 BR-014 Verified partners    Only partners with a current verification and an approved role          Proposed
 only                        can go on duty or be assigned. Suspension or deactivation takes
                             effect immediately.

 BR-015 Kit cold chain       Kits for home visits are packed no earlier than a set time before       Open on time limit
                             the slot and carried in insulated bags (Section 11).

 BR-016 Ratings              Only after a completed service. Moderation and removal rules to         Open
                             be agreed.

 BR-017 Offers               Each offer has eligibility, dates, hubs, services, usage limits and     Open configuration
                             stacking rules.

 BR-018 Operational          A hub closure, menu pause, zone pause or stock-out blocks new           Proposed
 pause                       confirmations and shows the customer a clear message.

 BR-019 Audit                Changes to prices, menus, stock, zones, policies, refunds,              Proposed
                             partner approvals and access log who, when and what changed.

   Policy Readiness Summary (7 Proposed Baseline Rules · 12 Configurable Open Parameters)
   Seven foundational integrity rules (BR-004, BR-006, BR-007, BR-012, BR-014, BR-018, BR-019) are locked as
   proposed baselines; twelve operational parameters cross reference Section 20 (OD 01 to OD 23) for M1/M2 sign off
```
