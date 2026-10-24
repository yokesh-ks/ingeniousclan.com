# Contributing

## Branch Protection
The `main` branch is protected. Direct pushes to `main` are not allowed. All changes must go through a Pull Request (PR).

### Workflow
1. Create a feature branch from `main` (`git checkout -b feature/your-feature`)
2. Make your changes and commit
3. Push the branch to origin (`git push -u origin feature/your-feature`)
4. Open a Pull Request against `main`
5. Get required reviews/approvals (if configured)
6. Merge via PR after checks pass

### Enforcement
To enforce this on GitHub, configure Branch Protection Rules for `main` with:
- Require a pull request before merging
- Restrict pushes that create files
- Optionally require status checks and reviews
- Do not allow force pushes or branch deletions

For GitHub repos, set via Settings → Branches → Branch protection rules.
