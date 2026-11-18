---
question: "Which of the following are requirements to publish an action to GitHub Marketplace?"
documentation: "https://docs.github.com/en/actions/how-tos/create-and-publish-actions/publish-in-github-marketplace"
---

- [x] The action must be in a public repository
> The documentation states that the action must be in a public repository.
- [x] The `name` in the action's metadata file must be unique and cannot match an existing Marketplace action or a user or organization on GitHub
> The documentation lists a unique `name` in the metadata file as a requirement.
- [x] The person publishing must use two-factor authentication
> The documentation states that publishing requires you to use two-factor authentication.
- [ ] The repository must be owned by an organization
> Anyone can publish an action in GitHub Marketplace.
- [ ] The repository must contain a workflow file in `.github/workflows`
> The documented requirements list a single action metadata file (`action.yml` or `action.yaml`) at the root of the repository, not a workflow file.
