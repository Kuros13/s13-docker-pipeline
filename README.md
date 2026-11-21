# s13-docker-pipeline

## Build the Docker image on every push and pull request

GitHub Actions runs the Docker build on each push and pull request using the
GitHub-hosted `ubuntu-latest` runner. Pushes publish
`dockerhub-tokens13/devopseasylearning:latest` to Docker Hub; pull requests build
locally without publishing. GitHub-hosted runner usage is free within the
allowance for your account and repository visibility; private repositories may
have usage limits.

The repository must contain a `Dockerfile` in its root for the build to pass.

Before publishing, add these repository secrets under **Settings > Secrets and
variables > Actions**:

- `DOCKERHUB_USERNAME`: `dockerhub-tokens13`.
- `DOCKERHUB_TOKEN`: a Docker Hub access token with permission to push images.

Workflow: [`.github/workflows/docker-build.yml`](.github/workflows/docker-build.yml)
