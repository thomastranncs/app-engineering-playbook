
# Engineering Basic Checklist

Use this checklist to ensure your project meets NCS Engineering Fundamentals and industry best practices.

---

## 1. Source Control
- [ ] Default target branch (e.g., `main`) is protected/locked.
- [ ] All merges are performed via Pull Requests (PRs).
- [ ] PRs reference related work items (e.g., Jira tickets).
- [ ] Commit messages are clear and consistent (describe what and why).
- [ ] Branch naming follows conventions (see [branching](./source-control/branching.md)).
- [ ] Repository structure is documented.
- [ ] No secrets in commit history or public code ([see secret scanning](./dev-sec-ops/secret-scanning.md)).
- [ ] Follows [Git Flow or GitHub Flow](./source-control/README.md) as appropriate.

## 2. Work Item Tracking
- [ ] All work is tracked in Jira (or equivalent system).

## 3. Testing
- [ ] Unit tests cover all critical components (>90% if possible).
- [ ] Integration/end-to-end tests are implemented and run regularly.
- [ ] Test results are visible and actionable.
- [ ] See [testing guide](./testing/README.md).

## 4. CI/CD
- [ ] CI runs automated build and tests on every PR.
- [ ] CD deploys to a replica/staging environment before merging to main.
- [ ] Main branch is always shippable.
- [ ] See [CI](./CI-CD/continuous-integration.md) and [CD](./CI-CD/continuous-delivery.md) docs.

## 5. Security
- [ ] Access is granted on a least-privilege basis.
- [ ] Secrets are stored securely (never in code).
- [ ] Data is encrypted in transit (and at rest, if required).
- [ ] Passwords are hashed and never stored in plain text.
- [ ] System is logically segmented for security (separation of concerns).
- [ ] See [security guide](./security/README.md).

## 6. Agile/Scrum
- [ ] Daily standups are run by a Process Lead (fixed or rotating).
- [ ] Agile process is clearly defined and documented.
- [ ] Dev Lead, PO, and others manage and refine the backlog.
- [ ] Working agreement is established with the customer.

## 7. Design Reviews
- [ ] Design review process is included in the Working Agreement.
- [ ] Major components are reviewed and alternatives documented.
- [ ] Stories/PRs link to design documents.
- [ ] Each user story includes a design review task (assigned/removed during sprint planning).
- [ ] Project advisors are invited to design reviews or provide feedback.
- [ ] Customer-required reviews are identified and planned.
- [ ] Non-functional requirements are documented.
- [ ] Risks and opportunities are logged.

## 8. Code Reviews
- [ ] Team agrees on the purpose and process of code reviews.
- [ ] Code review checklist or process is established.
- [ ] Minimum number of reviewers (usually 2) enforced for PR merges.
- [ ] Linters, code analyzers, and tests are required for PR merges.
- [ ] Quick review turnaround is enforced.
- [ ] See [code review process](./code-reviews/README.md).

## 9. Retrospectives
- [ ] Retrospectives are held each sprint or week.
- [ ] 1-3 improvement experiments are identified and tracked.
- [ ] Experiments have owners and are added to the backlog.
- [ ] Longer retrospectives are held for milestones and project completion.

## 10. Engineering Feedback
- [ ] Team submits feedback on blockers and improvements.
- [ ] Suggestions are incorporated into the solution.
- [ ] Feedback is detailed and actionable.

## 11. Developer Experience
Developers should be able to:

- [ ] Build/compile the source without errors.
- [ ] Run all automated tests (unit, integration, e2e).
- [ ] Start the solution end-to-end in a local or test environment.
- [ ] Debug the solution (set breakpoints, step through code, inspect variables).
- [ ] Use local development configuration (e.g., `.env`, `appsettings.development.json`).
