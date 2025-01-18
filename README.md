
# Jenkins Setup with Pre-installed Plugins and User Roles

## Pre-installed Plugins:

- Git 5.7.0
- Workflow Aggregator: 600.vb_57cdd26fdd7
- Configuration as Code: 1915.vcdd0a_d0d2625
- Matrix Authorization Strategy:** 3.2.3
- Job DSL: 1.90
- Allure Jenkins Plugin: 2.32.0
- Credentials: 1405.vb_cda_74a_f8974
- Docker Plugin: 1.7.0
- Email Extension: 1866.v14fa_6d201654
- SonarQube Scanner: 2.17.3
- Slack Notification: 751.v2e44153c8fe1
- HTML Publisher: 1.37
- GitHub Integration: 1.40.0
- Prometheus Metrics: 801.v98e119d8eeda_
- NodeJS Plugin: 1.6.2

## Predefined User Roles:

Three user roles are configured, each with matching usernames and passwords:

- **Admin:**
  - Username: `admin`
  - Password: `admin`
  - Permissions: Full administrative access.

- **Developer:**
  - Username: `developer`
  - Password: `developer`
  - Permissions: Read and build permissions.

- **Viewer:**
  - Username: `viewer`
  - Password: `viewer`
  - Permissions: Read-only access.

## Usage Instructions:

 1. Pull the Docker Image:


```bash
docker pull cuxuanthoai/jenkins-jcasc:latest
```

### 2. Run the Jenkins Container:

```bash
docker run -d -p 8080:8080 -p 50000:50000 \
  -v jenkins_data:/var/jenkins_home \
  cuxuanthoai/jenkins-jcasc:latest

```

This command starts a Jenkins instance accessible at `http://localhost:8080`.

## Security Configuration:

The Jenkins instance is configured with a **local security realm** and a **project-based matrix authorization strategy**, ensuring appropriate access levels based on user roles.

This markdown format includes all the necessary information in a structured manner, including plugins, roles, usage instructions, and security configuration.
