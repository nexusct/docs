# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this repository, please report it privately to help us address the issue before it can be exploited.

### How to Report

**Do not** open a public GitHub issue for security vulnerabilities.

Instead, please report security issues by emailing: **security@nexusct.com**

When reporting, please include:

- A description of the vulnerability
- Steps to reproduce the issue
- Potential impact of the vulnerability
- Any suggested fixes or mitigations (if applicable)

We will acknowledge receipt of your report within 48 hours and will work with you to understand and address the issue promptly.

## Security Best Practices

This documentation site follows these security best practices:

### 1. No Secrets in Version Control

- **Never commit** API keys, passwords, tokens, or other sensitive credentials to the repository
- All sensitive configuration must use environment variables
- Use `.env.example` with placeholder values only; never commit actual `.env` files

### 2. Environment-Based Configuration

- Production deployments should use Mintlify's environment variable management
- All API keys and tokens must be stored as environment variables
- Configure secrets through the Mintlify dashboard for production deployments

### 3. Dependency Management

- Keep dependencies up to date to patch known vulnerabilities
- Regularly update the Mintlify CLI: `npm i -g mintlify@latest`
- Monitor security advisories for the Mintlify platform

### 4. Content Security

- MDX content is sanitized by Mintlify's rendering engine
- Avoid using `dangerouslySetInnerHTML` or inline scripts in MDX files
- External links in documentation should use HTTPS where possible

### 5. Access Control

- Limit repository access to authorized team members
- Use GitHub's branch protection rules for the `main` branch
- Require pull request reviews before merging changes

## Supported Versions

We support the latest version of this documentation site. Security updates are applied to the `main` branch.

## Third-Party Services

This documentation site integrates with:

- **Mintlify** - Documentation hosting and rendering platform
- **GitHub** - Source code repository and deployment automation

Please ensure your accounts with these services use:
- Strong, unique passwords
- Two-factor authentication (2FA)
- Appropriate access controls

## Disclosure Policy

When we receive a security report:

1. We will confirm receipt within 48 hours
2. We will assess the issue and determine severity
3. We will develop and test a fix
4. We will deploy the fix to production
5. We will credit the reporter (unless they prefer to remain anonymous)

Thank you for helping keep NexusCT documentation secure.
