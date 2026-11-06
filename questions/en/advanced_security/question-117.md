---
question: "Push protection is enabled on a repository. A developer saves an Alibaba Cloud access key ID in `deploy.cfg` and the matching access key secret in `notes.txt`, commits both files, and runs `git push` to the upstream repository. What happens?"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/code-security/reference/secret-security/secret-scanning-scope#detection-of-pattern-pairs"
---

- [ ] Push protection blocks the push, because both files are in the same `git push`.
- [ ] Push protection allows the push, because Alibaba Cloud keys are not a supported provider pattern.
- [x] Push protection allows the push, because the ID and secret are in separate files.
> See the [secret scanning docs](https://docs.github.com/en/enterprise-cloud@latest/code-security/reference/secret-security/secret-scanning-scope#detection-of-pattern-pairs) on detection of pattern pairs.