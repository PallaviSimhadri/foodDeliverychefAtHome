# BRD-FD-001 · Section 7: Order and booking lifecycle

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
                                                                     4A. FOOD ORDER FULFILMENT
                                                                     Hub Accepts   → Kitchen Cooks & Ready → Rider
                                                                     Assigned   → Picked Up → Delivered (OTP / Photo PoD)
      1.Zone & Capacity    2.Checkout Hold     3.Gateway Verified                                                                  5.Completed
      Check Hub, Stock,    Hold Kits & Chef     Reservation Fixed;                                                               Tax Invoice Issued;
       Chef / Rider Slot   (10m Timer Gate)    Price Snapshot Set                                                                Ratings & Support
                                                                                                                            (Hold Expired   → Auto Release)
                                                                     4B. FOOD WITH CHEF FULFILMENT
                                                                     Hub Packs & Seals Kits  → Chef Collects & Travels →
                                                                     Arrival Kit Check + Customer Visit OTP → Cooks

   Figure 7.1 — Order & Booking Lifecycle State Flow (Hold-Before-Payment, Gateway Verification & Doorstep Visit OTP Gate)

The customer pays only after the kits and chef time are held, the hub sees an order only after payment is verified, and
a chef visit starts only after the customer's visit OTP confirms the chef and the kits.
```
