# BRD-FD-001 · Section 17: Assumptions, constraints and out of scope

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
17.1 Assumptions

   The client owns and runs the hubs, kits, recipes, partners and kitchen operations.
   The client supplies menu content, photos, ingredients, allergens, serving sizes, prices, recipes and policy text.
   The client verifies chefs and riders (ID and background checks) before they are approved in the platform.
   The client names owners for operations, finance, support, food safety, customer and partner safety, data privacy
   and launch approval.
   The client owns third-party accounts (Section 16) and pays their running costs.
   Hub staff keep stock, daily kit plans, availability and statuses up to date, because the platform's promises depend
   on them.
   Partners have a smartphone that meets the agreed minimum and a mobile data connection.

17.2 Constraints

   Final scope and launch date depend on the decisions in Section 20 and on third-party capabilities.
   Live tracking and ETAs depend on phone permissions, network quality and the chosen map provider. Background
   location on Android and iOS is subject to store review.
   There is no fixed maximum number of hubs, but the client must give launch and peak volume forecasts so capacity
   can be tested.

17.3 Out of scope unless added through change control

   A marketplace for outside restaurants or independent chefs.
   Automated ingredient purchasing, supplier portals or vendor bidding.
   Partner payouts, payroll, HR, attendance, background-check processing, or full accounting or ERP integration. The
   Partner app shows earnings but does not pay them.
   Multi-drop route optimisation, subscriptions, loyalty wallet, memberships and referrals.
   Kitchen hardware, POS terminals, IoT sensors, weighing scales and kitchen display screens.
   Franchise billing, white-labelling for other brands, and operations outside India.
   Any integration not listed in Section 16.

            IN-SCOPE PLATFORM DELIVERABLES                          CLIENT-OWNED OPERATIONS & DATA                          OUT OF SCOPE (CHANGE CONTROL)
             • Customer App + Role-Based Partner App                • Physical Hubs, Kitchens, Kits & Cold Chain       • External Restaurant / Independent Chef Marketplace
               • Web Operations Dashboard (4 Roles)                 • Partner ID / Background Checks & Payouts           • Supplier Portals, ERP, Payroll & Partner Payouts
         • Holds, Kits, Orders, Slots, Payments, Tax Invoices    • Menu Catalogue, Allergens, Recipes & GST/FSSAI       • Multi-Drop Routing, Subscriptions, Wallets, Loyalty
        • Earnings View Only; 1-Hub Pilot & Store Submission    • All 3rd-Party Cloud, Gateway, SMS & Store Accounts   • Kitchen IoT/POS Hardware & Non-India Operations

   Figure 17.1 — Scope Boundary Matrix: Platform Build Scope vs. Client Operational Ownership vs. Excluded Change-Control
                                                           Items
```
