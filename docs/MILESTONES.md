# Milestones
Only mark work complete when its exit criteria have been verified.

| Stage | Deliverable | Exit criteria | Status |
| --- | --- | --- | --- |
| 0. Foundation | Repository, instructions, collaboration process | Foundation PR reviewed; local tool inventory supplied | In progress |
| 1. Scope and design | Page map, approved plans, brand assets, billing decision | Owner confirms public content and launch scope | Pending |
| 2. Public website | Responsive original pages with accurate offers | Desktop/mobile review; links and forms checked; no unsupported claims | Pending |
| 3. Staging deployment | Reproducible deployable package | Correct account serves a unique test page; HTTPS valid; staging access controlled | Pending |
| 4. Orders and payments | Chosen billing solution and Paystack test integration | Success, failure, cancellation, duplicate webhook and amount mismatch cases checked | Pending |
| 5. Portal and operations | Customer access, invoices and staff workflow | Access isolation and account recovery tested; existing service records reconciled | Pending |
| 6. Automation | WHM integration; registrar integration if selected | Test account lifecycle verified; retries do not duplicate services; manual recovery documented | Pending |
| 7. Launch | Deployment, recovery procedure and monitoring | Owner reviews release; production backup/rollback prepared; end-to-end checks pass | Pending |

## Immediate task
Open this branch in Antigravity and inventory local tool versions using docs/WORKFLOW.md. Report missing tools before installing anything. In parallel, gather the logo, brand colours and current approved hosting offers.

## Scope notes
A public website release can precede billing automation if ordering behaviour is clearly described. Skipping preservation of the disposable demo does not waive recovery planning for new production data or customer services.
