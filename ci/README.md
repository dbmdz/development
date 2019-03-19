# `.gitlab-ci.yml` skeleton

The `.gitlab-ci-base.yml` configuration is a skeleton for a generic GitLab CI 
configuration that can be included in various repositories.

# Usage

This generic GitLab CI configuration can be included in a project-specific
GitLab CI configuration via:

```yml
include: "https://raw.githubusercontent.com/dbmdz/development/master/ci/gitlab-ci-base.yml"
```

# Variables

The following GitLab CI environment variables needs to be set:

| Variable                          | Description
| --------------------------------- | -----------
| `BUILD_IMAGE_ANSIBLE_MAVEN_JDK`   | Name of OpenJDK 8 Docker Image
| `BUILD_IMAGE_ANSIBLE_MAVEN_JDK11` | Name of OpenJDK 11 Docker Image

# Limitations

Known limitations are:

* Sonar checks are currently not supported
* Publishing snapshots or releases to Nexus are not supported