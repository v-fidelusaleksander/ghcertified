---
question: "Copilot cloud agent automatically validates the code it generates before it completes a pull request. Which checks does it perform by default?"
documentation: "https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations"
---

- [x] CodeQL analysis, to identify code security issues
> This validation does not require a GitHub Advanced Security, Code Security, or Secret Protection license.
- [x] Checking newly introduced dependencies against the GitHub Advisory Database
> Dependencies are checked for malware advisories and for vulnerabilities with a CVSS rating of High or Critical.
- [x] Secret scanning, to detect leaked secrets
- [x] Copilot code review, to get a second opinion on the code
- [ ] Dynamic application security testing (DAST) against a deployed preview environment
> The built-in validation does not deploy or test a running application.
- [ ] Manual review by a member of the repository's security team
> The automated validation does not depend on a human. A human still reviews the resulting pull request. You can find the details of the analysis in the session log, and you can disable individual validation tools in the cloud agent settings.
