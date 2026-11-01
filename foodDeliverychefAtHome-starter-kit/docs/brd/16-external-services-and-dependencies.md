# BRD-FD-001 · Section 16: External services and dependencies

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The client opens and owns every third-party account below, so the platform keeps working whoever maintains it later.

Payment gateway: UPI, cards, net banking, wallets, refunds and settlement reports. To confirm: Provider                  Client Owned
choice; client completes merchant onboarding and KYC.

OTP and SMS: Sign-in for customers and partners, and transactional SMS. To confirm: Provider, DLT sender ID              Client Owned
and templates.

Maps and location: Address pinning, service zones, distance, navigation and ETAs. To confirm: Provider and               Client Owned
expected usage.

Push notifications: Alerts in the Customer and Partner apps. To confirm: Client-owned Google and Apple                   Client Owned
developer credentials.

WhatsApp messaging (optional): Order updates and support messages. To confirm: Provider, template approval,                   Optional
opt-in.

Masked calling (optional): Calls between customers and partners without sharing numbers. To confirm: Provider                 Optional
and per-minute usage.

Delivery company (optional): Third-party riders instead of, or alongside, rider partners on the Partner app. To confirm:           OD-06
In-house, third-party or both (OD-06); the company's status and proof features.

Email: Invoices, reports and dashboard sign-in. To confirm: Sending domain and provider.                                 Client Owned

App stores: Publishing the Customer and Partner apps on Google Play and the App Store. To confirm: Client-               Client Owned
owned developer accounts and store listings for both apps.

Hosting and monitoring: Running the platform, backups and alerts. To confirm: Client-owned cloud account                 Client Owned
and access.

Usage-based services (SMS, maps, WhatsApp, calling, hosting) carry running costs that the client pays directly.
```
