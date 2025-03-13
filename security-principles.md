# Sequin security and privacy engineering principles

## Overview

This document establishes the security and privacy engineering principles adopted by Sequin Labs, Inc. for all information system implementation efforts. Rather than maintaining extensive custom documentation, we align with industry-standard frameworks while adapting them to our specific needs.

## Security engineering standards

Sequin adopts the OWASP Proactive Controls as our primary security engineering reference. All software developers and system designers must adhere to these controls in their implementation work.

### Primary reference

- [OWASP Proactive Controls](https://owasp.org/www-project-proactive-controls/)

This framework provides concrete guidance on implementing our required secure-by-design principles:

1. Minimize attack surface area
2. Establish secure defaults
3. The principle of Least privilege
4. The principle of defense in depth
5. Fail securely
6. Don't trust services
7. Separation of duties
8. Avoid security by obscurity
9. Keep security simple
10. Fix security issues correctly

### Supplementary security resources

For additional technical guidance, developers may reference:

- [OWASP Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

## Privacy Engineering Standards

Sequin adopts the NIST Privacy Framework Core as our privacy engineering reference. All software developers and system designers must incorporate these principles in their implementation work.

### Primary Reference

- [NIST Privacy Framework](https://www.nist.gov/privacy-framework)

This framework provides practical guidance on implementing our required privacy-by-design principles:

1. Proactive not Reactive; Preventative not Remedial
2. Privacy as the Default Setting
3. Privacy Embedded into Design
4. Full Functionality – Positive-Sum, not Zero-Sum
5. End-to-End Security – Full Lifecycle Protection
6. Visibility and Transparency – Keep it Open
7. Respect for User Privacy – Keep it User-Centric

## Implementation requirements

All Sequin software developers must:

1. Review the referenced frameworks as part of onboarding
2. Apply these principles from the earliest design phases
3. Adhere to Sequin coding standards throughout the development cycle
4. Participate in security and privacy reviews

## Exceptions and adaptations

Any exceptions to these principles must be documented and approved by the CEO. As Sequin evolves, we will periodically review these principles and may incorporate additional company-specific guidance.

## Maintenance

This document will be reviewed annually to ensure ongoing alignment with industry best practices and Sequin Labs' evolving needs.

Last Updated: March 12, 2025
