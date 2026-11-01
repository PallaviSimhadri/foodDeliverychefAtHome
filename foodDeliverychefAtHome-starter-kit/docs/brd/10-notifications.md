# BRD-FD-001 · Section 10: Notifications

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Each event below alerts the listed people; partners receive alerts in the Partner app, and SMS or WhatsApp to
customers needs their consent.

 Event                                        Customer      Chef     Rider       Hub manager      Channel

 Payment success or failure                   Yes           –        –           –                Push, SMS

 Order or booking confirmed                   Yes           –        –           Yes              Push, SMS or WhatsApp,
                                                                                                  dashboard

 Hub rejects or cannot fulfil                 Yes           –        –           Yes              Push, SMS

 Chef assigned or changed                     Yes           Yes      –           –                Push

 Delivery assigned                            –             –        Yes         Yes              Push with sound,
                                                                                                  dashboard

 Booking reminder (day before & 2h before)    Yes           Yes      –           –                Push, SMS or WhatsApp

 Kits not ready 30m before chef leaves        –             Yes      –           Yes              Push, dashboard

 Chef en route and arrived                    Yes           –        –           Yes              Push

 Food ready for pickup                        –             –        Yes         Yes              Push, dashboard

 Rider picked up and arriving                 Yes           –        –           –                Push

 Delivered or visit completed                 Yes           –        –           Yes              Push, invoice by SMS or
                                                                                                  email

 Delay beyond promised window                 Yes           –        –           Yes              Push, SMS

 Cancellation                                 Yes           Yes      Yes         Yes              Push, SMS

 Refund started and completed                 Yes           –        –           –                Push, SMS

 Low kit stock                                –             –        –           Yes              Dashboard, email

 Partner approved, suspended or               –             Yes      Yes         Yes              SMS, push, dashboard
 deactivated

 SOS raised by a customer or partner          –             –        –           Yes + safety     Push, SMS, phone call
                                                                                 contact

Timings such as the reminder and kit-readiness alerts are configurable by the super admin. Chef and rider columns
refer to the partner on that job.

   Notification Delivery & Regulatory Governance
   All customer SMS alerts require DLT-registered sender IDs and approved templates (Section 15), while WhatsApp
   notifications require explicit customer opt-in (FR-CUS-018) and city/hub feature activation (FR-ADM-013). Critical
   operational events — such as delivery assignments (FR-PTR-005), 30-minute kit-readiness warnings, and SOS
   escalations (UAT-13) — trigger immediate audible dashboard or phone alerts.
```
