# Security Policy

## Supported Versions

| Repository | Supported |
|---|---|
| `one-day-website` (Golden Template) | Current `main` only |
| `pyle-stone` and other client sites | Current `main` only |
| `ccglabs-business-brain` | Current `main` only |

Older releases are not patched. If you are using a pinned or forked version, please upgrade to `main`.

## Reporting a Vulnerability

**Do not file a public GitHub issue for security vulnerabilities.**

Email **brian.reich@thecoresolution.com** with:
- A description of the vulnerability and affected repository
- Steps to reproduce or a proof-of-concept (if safe to share)
- Your assessment of impact and severity

You will receive a response within **3 business days** acknowledging the report. CCG Labs is a small operation — please allow up to **14 days** for a fix or mitigation to be deployed.

Public disclosure is welcome after a fix is in place, or after 90 days if no fix is forthcoming and you have notified us.

## Scope

The following are **in scope**:
- Lambda contact form handler (injection, auth bypass, data exposure)
- CloudFront distribution configuration (header injection, cache poisoning)
- GitHub Actions workflows (secret leakage, supply chain issues)
- Astro/Node.js dependencies with known CVEs

The following are **out of scope**:
- Denial-of-service attacks
- Issues requiring physical access to a device
- Social engineering attacks targeting CCG Labs staff
