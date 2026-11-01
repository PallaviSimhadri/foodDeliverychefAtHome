# BRD-FD-001 · Section 12: Data and catalogue management

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The client owns all business data below and names who keeps each record current; technical data design is in the
solution architecture.

 Record                       Minimum information                                                          Kept current by

 City                         Name, state, invoicing entity and tax registration, default prices and       Super admin
                              policies, support contacts.

 Hub                          ID, name, city, address, contact, hours, status, services, service zone,     Super admin
                              capacity, food licence number.

 Dish                         Name, description, photos, ingredients, allergens, dietary labels, serving   Menu owner
                              size, price by level, active dates, services.

 Kit                          Kit ID, linked dish and version, components and quantities, storage          Menu owner, Hub
                              instructions, shelf life, reorder level.                                     manager

 Daily kit plan               Number of each kit the hub will have for each future date, used for chef     Hub manager
                              bookings.

 Recipe                       Approved steps, portion standard, prep and cook time, hygiene notes.         Menu owner
                              Visible to authorised roles only.

 Inventory movement           Receipt, hold, reservation, use, release, transfer, write-off, adjustment,   Hub manager
                              reason, person and time.

 Partner                      Profile, photo, contact, role or roles, verification status and date, home   Hub manager, Super
                              hub, shifts, availability, job history.                                      admin

 Customer                     Name, phone, addresses, consents, order history. Only what the service       Customer, Support
                              needs.

 Order or booking             Customer, address, hub, service, items, guest count, slot, prices fixed at   System
                              confirmation, payment, statuses, assignments, exceptions.

 Payment and refund           Gateway reference, amount, status, dates, reconciliation state, approvals.   System, Finance

 Invoice                      Number, entity, tax breakdown, customer details, date.                       System

 Support case, review &       Linked order, category, notes, owner, resolution, rating, moderation and     Support, Client safety
 incident                     incident history.                                                            owner

Before launch, the client fills a catalogue template for every dish and kit. Nothing is published to customers without
the menu owner's sign-off.
```
