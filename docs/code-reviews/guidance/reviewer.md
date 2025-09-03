
# Code Review Guidance for Reviewers

## The Reviewer's Role and Mindset

As a reviewer, you are a steward of code quality, maintainability, and team growth. Your goal is to:

- Ensure code is correct, secure, and maintainable.
- Help authors grow and share knowledge.
- Keep the codebase healthy and consistent.
- Foster a positive, collaborative culture.

## What to Look For in a Code Review

1. **Design:**
	- Is the code well-structured and appropriate for the system?
	- Does it follow architectural patterns and design principles?
2. **Functionality:**
	- Does the code do what it’s supposed to? Are requirements and acceptance criteria met?
	- Are edge cases and error conditions handled?
3. **Complexity and Readability:**
	- Is the code as simple as possible? Can it be made clearer or more concise?
	- Would another developer easily understand and maintain this code?
4. **Testing:**
	- Are there sufficient, effective automated tests (unit, integration, etc.)?
	- Are tests meaningful and do they cover new/changed logic?
5. **Naming:**
	- Are variable, class, and method names clear, consistent, and meaningful?
6. **Comments and Documentation:**
	- Are comments clear, necessary, and helpful? Is documentation updated?
	- Is the intent of complex code explained?
7. **Style and Consistency:**
	- Does the code follow the team’s style guide and conventions?
	- Is formatting consistent?
8. **Security and Safety:**
	- Are there any obvious security issues or unsafe practices?
	- Is sensitive data handled appropriately?

## How to Review Effectively

### 1. Prepare for the Review
- Read the PR description and related work items for context.
- Skim the overall change before diving into details.

### 2. Review Thoroughly, Prioritizing Major Issues
- Focus first on correctness, security, and design.
- Group minor issues (style, nits) and suggest fixes, but don’t block on them unless they are pervasive.

### 3. Give Respectful, Actionable Feedback
- Phrase feedback as suggestions, not commands (e.g., "Consider renaming..." or "Could we simplify this by...").
- Be specific about what needs to change and why.
- Suggest alternatives or improvements when possible.
- Focus on the code, not the person.

#### Example of Good Feedback:
> Consider extracting this logic into a helper method to improve readability and reduce duplication.

#### Example of Poor Feedback:
> This is wrong. Fix it.

### 4. Handle Disagreements and Pushback
- Distinguish between required changes and optional suggestions (e.g., use "nit:" for non-blocking comments).
- If you disagree, explain your reasoning and be open to discussion.
- If consensus cannot be reached, escalate respectfully (e.g., involve a tech lead).

### 5. Review Promptly and Communicate
- Respond to review requests in a timely manner (ideally within one business day).
- If you need more time, let the author know.
- Don’t let reviews block the team’s progress.

### 6. Encourage Learning and Growth
- Use reviews as opportunities for mentoring and knowledge sharing.
- Recognize good work and improvements.

## The Review Process: Step-by-Step

1. Read the PR description and related context.
2. Skim the diff to get a sense of the change.
3. Review each file, leaving comments and questions as needed.
4. Summarize your feedback and next steps (approve, request changes, or ask questions).
5. Follow up on responses and re-reviews until the PR is ready to merge.

## Example Reviewer Checklist

```
- [ ] Code meets requirements and acceptance criteria
- [ ] No obvious bugs, security, or performance issues
- [ ] Code is clear, maintainable, and well-structured
- [ ] Tests are adequate, meaningful, and passing
- [ ] Documentation and comments are updated if needed
- [ ] Feedback is constructive, actionable, and respectful
- [ ] Review completed promptly and communicated clearly
```

## Additional Tips

- Use "Approve" when the code is ready to merge, "Request changes" for blocking issues, and "Comment" for questions or suggestions.
- Use "nit:" for minor, non-blocking suggestions.
- If a PR is too large, ask the author to split it into smaller, focused changes.
- Praise good practices and improvements to encourage positive behavior.
