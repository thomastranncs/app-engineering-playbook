# Bicep Code Review Guidance

## Style Guide

### Bicep Coding Conventions

- **Naming:**
	- Use descriptive, meaningful names for resources, parameters, and variables.
	- Use camelCase for variables and parameters, and PascalCase for resource names.
- **Layout and Structure:**
	- Organize code logically: parameters, variables, resources, outputs.
	- Use comments to explain complex logic or intent.
	- Group related resources together.
- **Parameters and Variables:**
	- Use parameters for values that may change between deployments.
	- Set default values and use allowed values where appropriate.
	- Use variables to simplify complex expressions.
- **Resource Definitions:**
	- Use symbolic names for resources.
	- Reference outputs and properties using symbolic names, not hardcoded strings.
	- Use modules to encapsulate reusable components.
- **Outputs:**
	- Output important resource IDs, endpoints, or connection strings as needed.

### Secure Bicep Practices

- **Input Validation:**
	- Use allowed values and constraints for parameters.
	- Avoid using overly permissive values (e.g., 0.0.0.0/0 for IP ranges).
- **Secrets Management:**
	- Never hardcode secrets or credentials in Bicep files.
	- Use Azure Key Vault references for sensitive data.
- **Access Control:**
	- Apply least privilege to role assignments and access policies.
	- Use managed identities where possible.
- **Resource Security:**
	- Enable diagnostic logging and monitoring for resources.
	- Use secure defaults (e.g., HTTPS only, encryption at rest).
- **General Security:**
	- Keep modules and referenced templates up to date.
	- Review and test templates for security vulnerabilities.
	- Use template validation tools (e.g., `bicep build`, `bicep linter`).

## Code Analysis / Linting

- Use the Bicep linter to enforce style and best practices (`bicep build` and `bicep lint`).
- Address all warnings and errors before merging code.

## Build Validation

- Validate Bicep files in CI pipelines to prevent deployment of invalid or insecure templates.
- Use test deployments or what-if analysis to verify changes.

## Code Review Checklist

In addition to general code review best practices, consider the following Bicep-specific items:

- Are resource names, parameters, and variables clear and consistent?
- Are parameters validated with allowed values and constraints?
- Are secrets and sensitive data handled securely?
- Is least privilege applied to all access controls?
- Are modules used for reusable components?
- Are outputs meaningful and necessary?
- Are all linter warnings and errors addressed?
- Is the template free of hardcoded values that should be parameterized?
- Are secure defaults enforced for all resources?
- Is diagnostic logging enabled where appropriate?
- Are dependencies and references up to date?
