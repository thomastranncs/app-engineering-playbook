
# Code Review Guidance for Developers (Authors)

## The Author's Role and Mindset

As a code author, your responsibility is to make your changes easy to review, understand, and integrate. Your goals are to:

- Deliver high-quality, maintainable code.
- Communicate intent and context clearly.
- Collaborate constructively with reviewers.
- Help keep the codebase healthy and consistent.

## Best Practices for Authors

### 1. Prepare Your Change
- **Start with a clear goal:** Know what problem you are solving and why.
- **Keep changes small and focused:** Submit self-contained changes that address a single concern. Avoid mixing unrelated changes.
- **Write and update tests:** Ensure new/changed code is covered by meaningful tests.
- **Update documentation:** Revise docs, comments, and READMEs as needed.

### 2. Write a Great Pull Request (PR)
- **Use a descriptive title:** Start with the Jira ticket ID or work item ID, followed by a concise description of the change (e.g., `HMA-1234: Add authentication to login page`).
- **Write a detailed description:**
	- Explain what changed, why, and how.
	- Reference related issues or tickets, but provide enough context in the PR itself.
	- Use a checklist to clarify objectives and help reviewers focus on key areas.
- **Link work items:** Connect the PR to relevant tasks, stories, or issues.
- **Add reviewers:** Request reviews from teammates familiar with the code or domain, and consider including someone less familiar for a fresh perspective.
- **Annotate complex changes:** Add comments in the code to explain non-obvious logic or design decisions. For large PRs, provide an overview or guide to help reviewers navigate the changes.

### 3. Before Requesting Review
- **Ensure code compiles and passes all tests.**
- **Run linters and style checks.**
- **Rebase or merge with the base branch to resolve conflicts.**
- **Double-check for secrets or sensitive data.**

## Handling Reviewer Comments and Feedback

- **Be open to feedback:** Respond to all comments respectfully and promptly.
- **Address all feedback:** Make changes as needed, or explain why a suggestion is not being adopted (with clear reasoning).
- **Ask clarifying questions:** If a comment is unclear, ask for more details in the review thread.
- **Handle disagreements constructively:** Discuss and reach consensus. If a discussion stalls, consider a quick meeting to resolve it.
- **Create follow-up tasks:** If a comment is out of scope, create a follow-up work item or issue.

## Example Checklist for PRs

```
- [ ] Code compiles and passes all tests
- [ ] Follows style and linting guidelines
- [ ] PR description explains what, why, and how
- [ ] Linked to relevant work items or issues
- [ ] Added/updated tests and documentation
- [ ] All comments addressed or explained
```

## Example PR Description Template

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

- Use "draft" PRs for work in progress.
- If your PR is large, provide a guide or summary to help reviewers navigate it.
- Avoid force-pushing after review has started unless necessary—communicate if you do.
- Thank reviewers for their time and feedback.
