# BRD-FD-001 · Section 11: Trust, safety and food safety

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
A partner entering a customer's home with raw ingredients is the highest-trust moment in this business, so it needs
its own controls.

         1. PRE-VISIT VERIFICATION              2. HUB COLD-CHAIN & SEAL               3. ARRIVAL KIT CHECK & OTP             4. SOS & INCIDENTS
        • ID & Background Checked Partner      • Batch & Expiry Checked at Packing      • Chef Shows Sealed Kits at Door      • 1-Tap SOS in Both Apps
        • Super Admin Role Approval Gate        • Packed Within Cold-Chain Limit       • Customer Checks App Order List      • Alerts Hub + Safety Owner
       • Chef Photo & Verified Badge Shown      • Sealed Kits & Handover Logged      • Match→ Share Visit OTP (5-Try Lock)    • Direct 1-Tap Call to 112
      • Masked Calling & Active-Only Address     • Insulated / Chilled Bag Transit    • Mismatch → Report Issue (No OTP)     • Permanent Restricted Log

      Figure 11.1 — End-to-End Home-Visit Trust, Cold-Chain Kit Verification, Visit OTP Gate & SOS Escalation Architecture

11.1 Home-visit and partner safety

   Only partners with a current verification and an approved role can go on duty or be assigned (BR-014). The client
   runs the verification itself (ID and background checks).
   The customer sees the chef's name, photo and verified status before arrival.
   A visit starts only after the customer has checked the kits and the chef enters the customer's visit OTP, so the right
   chef is at the right home with the ordered kits. The code locks after 5 wrong tries and alerts the hub.
   Customers and partners both have an SOS button during active jobs. It alerts the hub and the client's named safety
   contact with the job, address and both parties' details, and offers a one-tap call to 112.
   Phone numbers between customers and partners are masked where the calling provider allows it. Customer
   addresses are shown to partners only during the active job.
   The client sets house rules for partners (dress code, conduct, what they may not do) and for customers (safe
   workspace, an adult at home). These are shown in the booking.

11.2 Food safety and kit handling

   Every dish lists its allergens and dietary labels, supplied and approved by the client.
   Kits for home visits are packed no earlier than a set time before the slot and carried in insulated or chilled bags.
   The hub checks and seals each kit against the booking and records the handover to the chef. At the home, the chef
   shows the sealed kits to the customer before cooking (arrival kit check).
   Expired or damaged kits cannot be packed. Kits with batch and expiry tracking are checked at packing.
   The chef confirms the client's hygiene checklist in the Partner app at the start and end of each visit.
   What happens to leftovers, packaging and cleaning after the visit must be agreed (OD-10).

11.3 Incident handling

   Any safety, hygiene or conduct complaint becomes a high-priority support case.
   The client names an owner who reviews incidents and decides on partner suspension or customer blocking.
   Incident records are kept with restricted access and are not deleted with an account.
```
