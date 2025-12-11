# CI
CI in CI/CD stands for Continuous Integration.

In simple terms:

Continuous Integration is the practice of frequently merging code changes from multiple developers into a shared repository, followed by automated builds and tests.

Why it matters:

Catches bugs early

Ensures the codebase is always in a working state

Makes integration simpler and faster

Supports rapid development workflows

CI usually includes:

Automatic building of the application

Running automated tests (unit, integration, etc.)

Static analysis or linting

If you want, I can also explain CD (Continuous Delivery / Deployment) or show how CI works in GitHub Actions, GitLab CI, Jenkins, etc.
# CD
CD in CI/CD stands for either:

✅ Continuous Delivery

or

✅ Continuous Deployment

Different teams use one or the other.

Continuous Delivery

The practice of automatically preparing every change for release, so the software is always in a deployable state.
A human typically approves the final release.

Key idea:

Code is automatically tested and packaged, but deployment to production is manual.

Continuous Deployment

The next step beyond Delivery: every code change that passes automated tests is automatically deployed to production with no human approval.

Key idea:

Fully automated code releases.
