# BRD-FD-001 · Section 15: Compliance considerations (India)

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The client owns legal and tax compliance and should confirm each item below with qualified advisers; the platform
then supports whatever they decide. This is a list of topics to confirm, not legal advice.

 Area                      What to confirm                                                Platform support

 Food licensing            FSSAI licence or registration for every hub, and what          Store and display each hub's licence
                           must be shown to customers in the app.                         number (FR-ADM-008).

 Tax and invoicing         GST treatment for delivered food and for the chef-at-          Tax rules and invoicing entity set per city
                           home service, which may differ; invoicing entity per state.    or state; invoice per order (FR-OPS-006).

 Personal data             Obligations under the Digital Personal Data Protection         Consent records, account deletion,
                           Act, 2023: notice, consent, purpose, retention, deletion       access controls, retention settings
                           and breach response.                                           (FR-CUS-019, NFR-006).

 Data location             Primary data is stored in India. Some providers, such as       Provider list with data locations, for
                           error monitoring or content delivery, may process data         advisers to approve.
                           elsewhere.

 Consumer protection       E-commerce consumer rules: seller details, grievance           Policy pages, grievance contact and price
                           officer, refund and cancellation policy, full price display.   breakdown before payment.

 Payments                  Use an RBI-authorised payment aggregator; refund               Gateway integration; no card data stored
                           timelines.                                                     (NFR-007).

 SMS and WhatsApp          DLT registration of sender IDs and templates for SMS;          Templates managed in the dashboard;
                           WhatsApp template approval and opt-in.                         consent recorded.

 Partner engagement        Employment or contractor terms, insurance, verification        Verification status and approval gate
                           and safety duties for chefs and riders.                        (BR-014, FR-ADM-006).

 App stores                Google Play and Apple App Store policies for both apps,        Built into app scope.
                           including account deletion, background location wording
                           and privacy labels.
```
