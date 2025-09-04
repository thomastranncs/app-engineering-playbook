
# Code Reviews

## Introduction

Code review is a collaborative process where someone other than the author examines code changes before they are merged into a shared branch. The primary goals are to improve code quality, share knowledge, and maintain a healthy, maintainable codebase.

---

## Why Do Code Reviews?

- **Improve Code Quality:** Identify and remove defects, enforce standards, and ensure best practices are followed before code is integrated.
- **Knowledge Sharing:** Expose team members to new patterns, technologies, and parts of the codebase, helping everyone learn and grow.
- **Shared Understanding:** Foster a shared understanding of the system and encourage collective ownership of the code.

---

## What to Look For in a Code Review

- **Design:** Is the code well-designed and appropriate for the system?
- **Functionality:** Does the code behave as intended and meet requirements?
- **Simplicity:** Can the code be made simpler or more readable?
- **Testing:** Are there sufficient and effective automated tests?
- **Naming:** Are variable, class, and method names clear and meaningful?
- **Comments:** Are comments clear, necessary, and helpful?
- **Style:** Does the code follow the team's style guide?
- **Documentation:** Is relevant documentation updated as needed?

---


## Best Practices

- Review every pull request or change before merging.
- Choose reviewers who are familiar with the code or domain.
- Provide constructive, actionable feedback.
- Keep reviews timely and respectful.
- Use code review tools to streamline the process.

---

## Code Review Strategies

Different strategies can be used depending on the team, codebase, and experience level of contributors:

- **Standard Pull Request Review:** The most common approach. Code is reviewed by one or more team members before merging. Suitable for most changes and contributors.
- **Pair Code Review (Recommended for Junior Developers):** Junior developers are encouraged to review code together with a more experienced developer. This approach provides real-time feedback, learning opportunities, and helps juniors understand standards and best practices.
- **Group Review:** For complex or high-impact changes, a group review session can be held to gather feedback from multiple stakeholders at once.
- **Self-Review:** Authors should always review their own code before requesting a review, catching obvious issues early.

Pair code review is especially valuable for onboarding, skill development, and ensuring that junior team members are supported in their growth.

---

## Resources & Related Documentation

- [Developer Code Review Guidance](guidance/developer.md)
- [Reviewer Code Review Guidance](guidance/reviewer.md)
- [Pull Request Template](pull-request-template.md)
- [C# Code Review Checklist](recipes/csharp.md)
- [Bicep Code Review Checklist](recipes/bicep.md)


