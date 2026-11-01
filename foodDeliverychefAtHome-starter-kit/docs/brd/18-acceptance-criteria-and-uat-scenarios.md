# BRD-FD-001 · Section 18: Acceptance criteria and UAT scenarios

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The platform is ready for the pilot when every scenario below passes in UAT, no critical or high defects remain open
(unless the client waives them in writing), and the named business owners sign off.

 UAT ID         Scenario and expected result                                                       Covers

 UAT-01         Admin creates a new city and hub with a service zone; it takes orders without      FR-ADM-001, FR-ADM-002,
                an app release.                                                                    NFR-004

 UAT-02         Customer at a serviceable address completes a Food Order from menu to              FR-CUS-003 to 013, FR-CUS-
                payment, kitchen, rider delivery with proof, and invoice.                          016, FR-HUB-003, FR-RID-001
                                                                                                   to 004, FR-OPS-006, 007

 UAT-03         Customer books a chef; the booking is offered and accepted only when slot,         FR-CUS-009, FR-HUB-004, BR-
                chef and kits fit the rules.                                                       008

 UAT-04         Chef partner collects verified kits, travels, shows the kits to the customer,      FR-HUB-006, FR-CHF-004 to
                enters the visit OTP, cooks and completes the visit. A customer who reports a      006, FR-CUS-014
                missing kit instead of sharing the OTP starts the hub's exception flow.

 UAT-05         Customer outside every zone cannot order and sees a clear message.                 FR-CUS-003, BR-003

 UAT-06         Minimum-order, guest-count, fee, offer and cancellation rules apply the same       FR-CUS-008, FR-CUS-010, BR-
                at cart, checkout and after the order.                                             002, BR-010, BR-017

 UAT-07         Kits are held at checkout, reserved on payment, used on cooking or packing,        FR-OPS-002, FR-OPS-009, FR-
                released on cancellation, and shown correctly in reports.                          HUB-007

 UAT-08         Many customers try to buy the last few kits, or book the same chef slot, at the    FR-OPS-009, FR-HUB-004, NFR-
                same time: no kit is oversold and no chef is double-booked.                        008

 UAT-09         Repeated payment attempts and duplicate gateway messages create one                FR-OPS-003, NFR-008
                order and one charge.

 UAT-10         Customer does not pay within the hold time: kits and chef time return to           FR-CUS-020, FR-OPS-009, FR-
                availability. A payment that arrives after expiry is re-held or refunded in full   OPS-010, BR-005
                automatically.

 UAT-11         Cancellation at each stage gives the refund the policy promises, and the           FR-CUS-017, FR-OPS-005, BR-
                refund is tracked to completion.                                                   010

 UAT-12         A chef or rider becomes unavailable; the hub reassigns or cancels and the          FR-HUB-004, FR-HUB-005, BR-
                customer is notified.                                                              012

 UAT-13         SOS from a customer or partner alerts the hub and the safety contact within 1      FR-CUS-015, FR-PTR-007, FR-
                minute.                                                                            HUB-012

 UAT-14         A chef-only partner sees no delivery jobs, a rider-only partner sees no home       FR-PTR-001 to 003, FR-ADM-
                visits, and an unapproved or deactivated partner cannot sign in or go on duty.     006, BR-014

 UAT-15         A hub manager cannot see another hub's data; a support agent cannot refund         Section 5, NFR-005
                above the limit.

 UAT-16         A price change after confirmation does not change the confirmed order or its       BR-007, FR-OPS-006
                invoice.

 UAT-17         Financial reports match order, payment and refund records for the test period.     FR-ADM-009, FR-ADM-010,
                                                                                                   Section 13.2

 UAT-18         Customer deletes their account; personal data is removed except records the        FR-CUS-019, NFR-006
                law requires keeping.

 UAT-19         Backup restore, monitoring alerts and support handover are demonstrated.           NFR-009, NFR-010, NFR-013

   End-to-End Requirement Traceability
   Scenarios UAT-01 to UAT-19 serve as formal Milestone Gates across M3, M4, M5 and M6 (Section 19), ensuring every
   functional, business-rule, and non-functional requirement is verified prior to pilot launch.
```
