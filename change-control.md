# Sequin code change control process

## Purpose

This document outlines the formal change control procedures for code changes within Sequin projects. These procedures ensure code quality, maintain security standards, and prevent unauthorized or problematic changes from affecting production systems.

## Scope

This process applies to all code changes that will be merged into production branches of Sequin repositories.

## Roles and responsibilities

- **Contributors**: Individuals making code changes
- **Reviewers**: Team members who review code changes (currently Anthony Accomazzo and Carter Pedersen)
- **Approvers**: Individuals with authority to approve changes (including Anthony Accomazzo for significant changes)
- **Deployment Team**: Individuals responsible for deploying approved changes to production environments

## Change control process

### 1. Development

1. Develop changes in a feature branch pulled from the latest main branch
2. We encourage smaller branches/PRs and stacking (We use Graphite to enable this)
3. Follow the established coding standards and style guidelines
4. Include appropriate unit and integration tests
5. Ensure all automated tests pass locally before submitting for review

### 2. Code review

1. Create a pull request (PR) with a clear description of the changes
2. Address all review comments and make necessary adjustments

### 3. Approval process

#### For regular changes
1. All automated tests must pass
2. All review comments must be addressed
3. Run the sign-off script (`make signoff`) to formally sign off on the pull request

#### For significant changes
Significant changes include:
- Architectural changes
- Changes to authentication or authorization systems
- Changes to data models or database schema beyond just adding and removing columns
- Changes affecting multiple components or services
- Security-sensitive modifications
- Changes to core business logic

For these changes:
1. **Final approval must come from Anthony Accomazzo**
2. All automated tests must pass
3. All review comments must be addressed
4. Run Sequin locally and perform end-to-end testing
5. Run the sign-off script (`make signoff`) to formally sign off on the pull request
6. May require additional security review for sensitive changes

### 4. Deployment

1. After approval, changes are merged into `main`
2. GitHub Actions builds containers on command
3. We deploy with a local command using Terraform
4. For open source components, GitHub Actions builds and releases new Docker images

### 5. Post-deployment verification

1. Monitor systems after deployment to ensure proper functioning
2. Document any issues encountered during deployment
3. For significant changes, conduct a post-implementation review

## Emergency change process

For critical bug fixes or security patches requiring immediate action:

1. The emergency change process may be used
2. Changes still require at least one reviewer
3. Changes must be documented after the fact
4. A post-implementation review must be conducted
5. Anthony Accomazzo must be notified of the emergency change as soon as possible

## Timeframes

We strive to move efficiently through the change control process:
1. Code reviews should be completed within hours when possible
2. The entire process from PR creation to deployment should typically be completed within several hours or a day
3. For more complex changes, the process should not exceed a couple of days
4. Emergency changes are addressed with appropriate urgency

## Compliance and enforcement

1. All changes must follow this process
2. Changes that bypass this process may be reverted
3. Regular audits of the change control process will be performed
4. Violations of the change control process will be addressed according to the Sequin Operations Security Policy

## References

This process complies with requirements outlined in the Sequin Labs, Inc. Operations Security Policy.

## Document control

- **Version**: 1.0
- **Last Updated**: 2025-03-12
- **Owner**: Anthony Accomazzo
