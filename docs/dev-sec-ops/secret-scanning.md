# Secret Scanning and Credential Management

To protect sensitive information and maintain compliance, all projects must ensure that secrets (such as API keys, passwords, tokens, and certificates) are never committed to source control.

## Why Secret Scanning?
- Prevents accidental exposure of credentials and secrets.
- Reduces risk of security breaches and data leaks.
- Supports compliance with industry standards and regulations.

## Best Practices
- Never store secrets in code repositories.
- Use environment variables or secure vaults (e.g., Azure Key Vault, AWS Secrets Manager) for secret management.
- Rotate secrets regularly and immediately after exposure.
- Review and remove secrets from commit history if found.

## Automated Secret Scanning
Use automated tools to scan for secrets before code is pushed or merged:
- **GitHub Advanced Security**: Built-in secret scanning for public and private repos.
- **TruffleHog**: Scans git history for secrets.
- **Gitleaks**: Detects hardcoded secrets in code and git history.
- **Pre-commit hooks**: Integrate secret scanning into your CI/CD pipeline.

## Responding to Exposed Secrets
1. **Revoke** the exposed secret immediately.
2. **Remove** the secret from all code and commit history.
3. **Rotate** the secret and update all dependent systems.
4. **Notify** your security team and follow incident response procedures.

---

For more on secure development, see the [Security Guide](../security/README.md).
