# `.gitlab-ci.yml` skeleton

The `.gitlab-ci-base.yml` configuration is a skeleton for generic GitLab CI
configuration that can be included in various repositories. It is currently
used at @dbmdz to build our Open Source projects on GitHub.

# Usage

This generic GitLab CI configuration can be included in a project-specific
GitLab CI configuration via:

```yml
include: "https://raw.githubusercontent.com/dbmdz/development/master/ci/gitlab-ci-base.yml"
```

# Variables

The following GitLab CI environment variables needs to be set:

## Group variables

| Variable                          | Description
| --------------------------------- | -------------------------------
| `BUILD_IMAGE_ANSIBLE_MAVEN_JDK`   | Name of OpenJDK 8 Docker Image
| `BUILD_IMAGE_ANSIBLE_MAVEN_JDK11` | Name of OpenJDK 11 Docker Image
| `SONATYPE_USERNAME`               | Username of Sonatype Repository
| `SONATYPE_PASSWORD`               | Password of Sonatype Repository

## Repository-wise variables

Each repository should define the following variables:

| Variable                          | Description
| --------------------------------- | ---------------------
| `CODECOV_TOKEN`                   | Token for Codecov API

If the environment variable `NO_PUBLISH` is set, then deploying artifacts to
Sonatype is disabled.