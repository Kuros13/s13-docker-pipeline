# s13-docker-pipeline

## Build the Docker image on every push and pull request

GitHub Actions runs the Docker build on each push and pull request using the
GitHub-hosted `ubuntu-latest` runner. The workflow builds the image but does not
publish it. GitHub-hosted runner usage is free within the allowance for your
account and repository visibility; private repositories may have usage limits.

The repository must contain a `Dockerfile` in its root for the build to pass.

Workflow: [`.github/workflows/docker-build.yml`](.github/workflows/docker-build.yml)
