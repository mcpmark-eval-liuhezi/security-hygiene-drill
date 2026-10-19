# Security Checklist

Quarter-end security hygiene checklist for this repository. Work through each item and record the date and owner for every check.

## 1. Dependency Updates

- [ ] Run `npm audit` / `pip-audit` / `dependabot alerts` review and triage all critical and high findings
- [ ] Review and merge all open Dependabot pull requests
- [ ] Update manifest and lockfiles to the latest patch versions
- [ ] Confirm no deprecated or unmaintained packages remain in the dependency tree
- [ ] Verify Dependabot version updates are configured for all ecosystems in use

## 2. Secret Handling

- [ ] Run secret scanning on the full commit history; confirm zero open alerts
- [ ] Review push protection rules and confirm they are enabled
- [ ] Remove any hardcoded credentials, tokens, or API keys from source
- [ ] Rotate any credentials that were exposed, even briefly
- [ ] Confirm required secrets live only in GitHub Actions secrets or a vault
- [ ] Add patterns for internal token formats to the secret scanning configuration

## 3. Code Scanning

- [ ] Confirm code scanning (CodeQL) analysis runs on every pull request
- [ ] Triage and resolve all open code scanning alerts
- [ ] Review the alert severities and confirm no critical or high alerts remain open
- [ ] Update the code scanning ruleset / query suite to the latest available
- [ ] Confirm results are routed to the team via security advisories or notifications

## Sign-off

| Item | Owner | Date | Status |
| ---- | ----- | ---- | ------ |
| Dependency updates | | | |
| Secret handling | | | |
| Code scanning | | | |
