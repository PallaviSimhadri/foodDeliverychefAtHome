# BRD-FD-001 · Section 19: Milestones, pilot launch and change control

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
Work runs in six milestones that match the solution architecture, and each starts only after the client approves the
gate of the one before.

        M1 · DISCOVERY          M2 · DESIGN & PATH          M3 · CORE OPS            M4 · FOOD ORDER          M5 · CHEF AT HOME             M6 · PILOT & LIVE
        Resolve OD-01..08;      All App/Web Screens;     Hubs, Zones, Catalogue,     Ordering, Holds, Pay,    Slots, Kit Packing, Visit   Full UAT, Sec/Load, 1-Hub
      City, Hubs, Tech Checks   Staging E2E Test Path    Kits, Stock, Roles, Audit   Kitchen, Rider Screens   OTP, SOS, Chef Screens       Pilot (2–4w)   → Public

      Gate: BRD & Arch Signed   Gate: Screens Approved   Gate: UAT-01, 07, 08 Pass   Gate: UAT-02,09,10,16    Gate: UAT-03,04,13,14,08     Gate: UAT & Launch Sign

            Figure 19.1 — Six-Stage Gated Delivery Roadmap from Discovery (M1) to One-Hub Pilot & Public Launch (M6)

1. M1 – Discovery and technical checks. Resolve OD-01 to OD-08; confirm launch city and hubs, roles, policies and
   integrations. Prove the riskiest technical pieces early.
   • Gate: this BRD signed; solution architecture approved.
2. M2 – Design and first working path. Screens for the Customer app, both Partner app roles and the dashboard,
   including exceptions. A test order travels end to end in a staging environment.
   • Gate: client approves key screens and flows.
3. M3 – Core operations. Cities, hubs, zones, settings, catalogue, kits, daily kit plans, stock, roles, partner onboarding
   and approval, audit trail.
   • Gate: UAT-01 passes; kit tests in UAT-07 and UAT-08 pass.
4. M4 – Food Order end to end. Customer app ordering, holds, payments, invoices, notifications, kitchen queue, and
   the rider screens of the Partner app.
   • Gate: UAT-02, UAT-09, UAT-10 and UAT-16 pass in staging.
5. M5 – Chef at home. Slots, chef holds, kit packing, visit OTP, SOS, and the chef screens of the Partner app.
   • Gate: UAT-03, UAT-04, UAT-13, UAT-14 and the chef tests in UAT-08 pass.
6. M6 – UAT, pilot and launch. Full UAT, security and load tests, restore drill, store submission of both apps and staff
   training. Then a pilot at one hub with invited customers for 2 to 4 weeks, with real but limited orders, before the
   public launch.
   • Gate: written UAT sign-off, pilot review and launch approval.

The pilot does not reduce the scope: every feature is live, only the audience is limited while real-world issues are
found and fixed.

   Change control
   Any feature, rule or integration not written in this document is a change request. Each request is assessed for its effect
   on scope and launch date and needs client approval before work starts. Milestone dates are set in the project plan
   once M1 is complete.
```
