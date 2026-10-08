# Project brief and architecture
Status: foundation planning, 2026-10-08. This repository does not yet contain a working application.

## Goal
Replace the existing demo with an original website, clear hosting offers, and a staged path to ordering, payments and customer service management.

## Confirmed project decisions
- Fresh build; no migration of the old demo code.
- GitHub holds source and documentation; Antigravity opens the local checkout.
- Paystack is the intended payment provider.
- A separate development hosting account has been created.
- Production deployment is a later milestone.

## Proposed component boundaries
| Component | Responsibility |
| --- | --- |
| Public website | Hosting plans, product information, contact and support entry points |
| Order and billing service | Authoritative prices, order states, invoices, verified payment records |
| Customer portal | Authenticated access to a customer's own services and invoices |
| Staff interface | Order review, support and audited administrative actions |
| Hosting integration | Server-side WHM operations after explicit enablement |
| Domain integration | Registrar availability/registration only after provider selection |

WordPress is not a requirement. Billing implementation remains undecided: evaluate a licensed maintained billing product versus a limited custom order system before building authentication and billing. No WHMCS licence or domain reseller provider has been confirmed. Do not present domain availability or automated registrations as functional before integration.

## Deployment constraints to verify
PHP and database management are available in the inspected hosting interface. PHP 8.1 was reported and 8.5 appeared in a selector; the effective development-account runtime and extensions remain unverified. Terminal is unavailable in the inspected account. Node.js Selector reports unavailable; Application Manager is visible but runtime support is unproven.

Build assets and dependencies locally or in CI; deploy a prepared package if the host cannot run build tools. Select exact runtime/framework versions only after compatibility validation. A public frontend may be built independently of billing.

## Open items
- Development URL currently showed a cPanel default page; account routing and HTTPS are unverified. User deferred SSL work.
- Verify available local Git, PHP, Composer, Node and npm versions.
- Confirm brand assets, current packages/prices, public contact information and launch scope.
- Choose billing approach and budget before transactional implementation.
- Identify hosting provider and operational support path before enabling automation.
- Repository visibility is currently public; owner plans to change it later. Keep documents and fixtures suitable for public viewing.

## Transactional design requirements for later milestones
Use server-authoritative amounts/currency; verify payment status server-side; validate webhook authenticity; handle retries and duplicate events idempotently. Never activate hosting solely from a browser redirect. Preserve an audit trail, reconciliation and a recoverable failed-provisioning state. Keep WHM credentials server-side and restrict permissions. Delay destructive automation until separately reviewed.
