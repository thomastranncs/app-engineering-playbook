# C# Code Review Guidance

## Style Guide

### C# Coding Conventions

- **Naming:**
	- Use PascalCase for class, method, and property names.
	- Use camelCase for local variables and method parameters.
	- Use ALL_CAPS for constants.
	- Prefix interfaces with 'I' (e.g., `IService`).
- **Layout and Spacing:**
	- Use four spaces per indentation level (no tabs).
	- Place opening braces on a new line for types and methods; same line for other blocks.
	- Use a single blank line to separate logically related code blocks.
- **Modifiers and Visibility:**
	- Order elements: public, protected, internal, private.
	- Use explicit access modifiers.
- **Expression and Statement Formatting:**
	- Use `var` when the type is obvious; otherwise, use explicit types.
	- Use object and collection initializers where possible.
	- Prefer string interpolation over string.Format or concatenation.
- **Other Best Practices:**
	- Use properties instead of public fields.
	- Use using statements for resource management.
	- Avoid magic numbers; use named constants or enums.
	- Comment code where necessary, but prefer self-explanatory code.

### Secure Coding Guidelines

- **Input Validation:**
	- Always validate and sanitize user input.
	- Use parameterized queries to prevent SQL injection.
- **Authentication and Authorization:**
	- Use strong authentication mechanisms.
	- Enforce least privilege for users and services.
- **Error Handling:**
	- Do not expose sensitive information in error messages.
	- Log exceptions securely; avoid logging secrets.
- **Data Protection:**
	- Use encryption for sensitive data at rest and in transit.
	- Store secrets in secure locations (e.g., Azure Key Vault).
- **Code Practices:**
	- Avoid hardcoding credentials or secrets.
	- Use secure libraries and frameworks.
	- Keep dependencies up to date.
- **Other Security Practices:**
	- Use secure defaults.
	- Regularly review and test for vulnerabilities.
	- Apply security patches promptly.

## Code Analysis / Linting

- Use analyzers and linters to enforce style and code quality rules.
- Recommended packages:
	- `Microsoft.CodeAnalysis.NetAnalyzers`
	- `StyleCop.Analyzers`
- Use a shared `common.props` file and reference it in all projects for consistent configuration.
- Use `.editorconfig` to customize and override rules as needed.
- Adopt the [Managed Recommended Rules](https://learn.microsoft.com/en-us/visualstudio/code-quality/managed-minimum-rules-rule-set-for-managed-code?view=vs-2022) as a minimum rule set.

## Automatic Code Formatting

- Configure code formatting rules in `.editorconfig`.
- Use IDE or command-line tools to auto-format code before committing.

## Build Validation

- Enforce code style and rules in CI pipelines to prevent non-compliant code from being merged.
- Ensure analyzers and StyleCop run as part of the build process.

## Enable Roslyn Support in VS Code

- Set `omnisharp.enableRoslynAnalyzers` to `true` in VS Code settings.
- Restart Omnisharp or VS Code after changing this setting.

## Code Review Checklist

In addition to general code review best practices, consider the following C#-specific items:

- Correct use of asynchronous programming (`async`/`await`, `Task.WhenAll`, `CancellationToken`)
- Concurrency: Are shared objects properly protected?
- Dependency Injection (DI): Is it used and set up correctly?
- Middleware: Is it configured properly?
- Deterministic resource release: Use `IDisposable` and the `using` pattern
- Avoid excessive short-lived objects and unnecessary boxing
- Proper exception handling: Catch specific exceptions, not just `Exception`
- Use NuGet for package management, not committed DLLs
- Appropriate use of LINQ
- Argument validation (e.g., [CA1062](https://learn.microsoft.com/en-us/dotnet/fundamentals/code-analysis/quality-rules/ca1062))
- Telemetry: Are metrics, tracing, and logging instrumented?
- Use the options design pattern for configuration
- Use constants/static classes for repeated strings
- Avoid magic numbers; use constants or enums
- Tests: Use Arrange/Act/Assert pattern and document accordingly
- Async method names should end with `Async`
- Use `Task.Delay` instead of `Thread.Sleep` in async methods
- Use cancellation tokens for async tasks
- Ensure sensible logging levels and minimum logging is in place
- Use correct access modifiers (internal, private, public)
- Use auto-properties appropriately
- Ensure thread safety for in-memory collections

