# BRD-FD-001 · Section 14: Non-functional requirements

> Extracted from `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). The PDF is the source of truth; if this text and the PDF disagree, the PDF wins.

```text
The targets below are proposed starting points so testing has something measurable; the client confirms them once
launch volumes are known (OD-17).

 ID & Area                Requirement                                                      Proposed target

 NFR-001 Platforms        Customer and Partner apps run on supported Android and           Android 10+, iOS 16+, last two versions
                          iOS versions, including entry-level Android phones common        of Chrome, Edge and Safari; minimum
                          among partners. The dashboard runs on current browsers.          partner phone agreed

 NFR-002 Performance      Menu, cart, order status, partner job lists and dashboard        Screens load in under 3 seconds on 4G
                          queues stay responsive at peak meal times.                       for 95% of requests

 NFR-003 Availability     The platform is available during operating hours, with           99.5% monthly uptime
                          maintenance outside peak meal times.

 NFR-004 Scale            New hubs and cities are added by configuration, with no app      Demonstrated by adding a hub in UAT
                          release.

 NFR-005 Security         Secure sign-in, role-based access, multi-factor sign-in for      Security review, access tests and an
                          dashboard users, encrypted traffic, protected secrets.           external penetration test pass before
                                                                                           launch

 NFR-006 Privacy          Collect only needed data; record consent; collect partner        Privacy notice and retention schedule
                          location only during active jobs; support data access and        approved
                          deletion requests.

 NFR-007 Payment          Card and UPI details are handled only by the gateway; the        Confirmed in gateway integration
 safety                   platform stores references and statuses, never raw card          review
                          data.

 NFR-008 Reliability      Retries, duplicate gateway messages and weak networks do         Retry, recovery and parallel-order tests
                          not create duplicate orders, charges or oversold kits.           pass

 NFR-009 Monitoring       Errors and privileged actions are logged; named staff get        Alert list and owners approved
                          alerts for failures, low stock, unacknowledged SOS and
                          stuck payments or refunds.

 NFR-010 Backup &         Regular backups with tested restores.                            At most 15 minutes of data lost;
 recovery                                                                                  service restored within 4 hours; restore
                                                                                           tested before launch

 NFR-011 Usability &      Readable text, clear errors, labelled controls and large touch   UX review and accessibility checklist
 access                   targets, suited to partners using the app on the move.           pass

 NFR-012 Localisation     Indian rupee, Indian date and phone formats, agreed launch       Language list approved
                          languages for both apps.

 NFR-013                  Logs, admin guides, release notes and a clear support and        Handover pack signed off
 Supportability           escalation process.

   Pre-Launch Verification Benchmark
   Every target in NFR-001 through NFR-013 maps directly to Milestone 6 (M6) readiness checks, including parallel-order
   concurrency testing (UAT-08), idempotency verification (UAT-09), and backup restore drills (UAT-19).
```
