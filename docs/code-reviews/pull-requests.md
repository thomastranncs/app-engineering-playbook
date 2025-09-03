# Pull Requests

## What is a Pull Request?

A pull request (PR) is a request to merge code changes from one branch into another (typically into the main branch). PRs enable code inspection, automated checks, and collaborative review before changes are integrated into the main codebase.

## General Process

1. Implement changes based on clear requirements and acceptance criteria.
2. Ensure code follows agreed conventions and passes all linters and tests.
3. Update or add tests and documentation as needed.
4. Create a pull request with a clear, descriptive title and detailed description.
5. Request reviews from appropriate team members.
6. Address feedback and update the PR as needed.
7. Merge only after all checks and reviews are complete.

## Best Practices

- **Keep PRs Small and Focused:**
	- Small PRs are easier and faster to review, less likely to introduce bugs, and easier to merge.
	- Each PR should address a single concern or feature.
- **Write Clear Titles and Descriptions:**
	- Explain the "what," "why," and "how" of your changes.
	- Reference related issues or tickets, but always provide context in the PR itself.
	- Use a template for consistency (see below).
- **Include Related Tests:**
	- Add or update tests to cover your changes.
	- Describe how you tested the changes, especially for infrastructure or UI changes.
- **Follow Conventional Commits:**
	- Use commit messages like `feat: add user authentication` or `fix(api): correct null reference bug`.
	- See [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/) for details.
- **Collaborate and Communicate:**
	- Respond to feedback promptly and respectfully.
	- Keep the PR up to date with the base branch as needed.
- **Don’t Break the Build:**
	- Ensure all checks pass before merging.
	- Avoid merging large, risky, or untested changes.

## Recommended Pull Request Template

```
## What?
Describe what changes are included in this PR.

## Why?
Explain the motivation or business/technical reason for these changes.

## How?
Summarize the approach, design decisions, or key implementation details.

## Testing?
Describe how the changes were tested (include test coverage, manual steps, screenshots, etc.).

## Anything Else?
Mention any follow-up work, known issues, or additional context.
```

## Additional Tips

- Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/) for commit messages.
- Keep PRs self-contained and avoid mixing unrelated changes.
- Use screenshots or logs for UI or infrastructure changes when helpful.
