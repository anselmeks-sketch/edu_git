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


Examples of CI
1. GitHub Actions running tests on every pull request
A team using GitHub pushes code or opens a PR → GitHub Actions automatically:
installs dependencies
builds the project
runs unit tests and linters
reports failures back inside the PR
This ensures nothing can be merged unless the CI pipeline passes.

2. Jenkins automatically building and testing a Java backend
A company using Jenkins configures it to:
monitor the main branch
trigger a build whenever new code arrives
run Maven/Gradle tests
generate test coverage reports
publish artifacts for the next pipeline stage
Developers get notified on Slack if the build fails.

3. GitLab CI running integration tests in Docker
A microservices team uses GitLab CI with a .gitlab-ci.yml file that:
starts services in Docker containers (API, DB, cache)
runs integration tests against those containers
reports results to the merge request
blocks merges if tests fail
This guarantees that services work together before merging.


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

Examples of CD
1. Continuous Delivery: Staging release in GitHub Actions
A SaaS team uses GitHub Actions so that whenever code is merged into the main branch:
the application is built and tested
a Docker image is created and pushed to a registry
the new version is automatically deployed to a staging environment
a human must press “Approve” to deploy to production
This keeps the product always ready for release without automatically pushing to prod.

2. Continuous Deployment: Auto-deploy to AWS using GitLab CI
A backend service uses GitLab CI with Infrastructure-as-Code. Every successful pipeline run:
builds the app
runs tests
updates the ECS/EKS cluster via Terraform
rolls out the new version automatically
No human approval is required—the service deploys to production continuously as long as tests pass.

3. Continuous Deployment: Frontend auto-deploy to Vercel/Netlify
A frontend React or Next.js app is connected to Vercel or Netlify.
Whenever code is pushed or a PR is merged:
the platform builds the app
runs tests (if configured)
deploys the new version globally to the CDN
instantly invalidates and replaces cached assets
Developers don’t run deployment commands at all; production updates happen automatically.
