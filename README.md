# Security Audit

Web application security audit to be performed once per quarter.

- [ ] Review latest OWASP Top 10
- [ ] Run automatic security checks
  - [ ] Mozilla Observatory: https://observatory.mozilla.org
  - [ ] Google CSP Evaluator: https://csp-evaluator.withgoogle.com/
  - [ ] Security header scanner: https://securityheaders.com/
  - [ ] Lighthouse (Chrome dev tools)
- [ ] Ensure encryption of data in transit (force SSL connections everywhere possible)
- [ ] Ensure encryption of data at rest (databases, harddrives, passwords, etc should be encrypted)
- [ ] Update all dependencies
  - [ ] Use LTS versions (Node.js, Ubuntu, etc)
- [ ] No vulnerabilities found in dependencies (GitHub and npm security reports, etc)
- [ ] Lock down ports (tcp, udp, etc)
  - [ ] Only open ports that are absolutely necessary
  - [ ] Only open the smallest subset of absolutely necessary IP addresses on each port
- [ ] Ensure strong authentication system
  - [ ] Study up on the latest authentication best practices
  - [ ] up-to-date and secure
  - [ ] Cookies, JWTs, private and public keys, web storage, etc all used correctly
- [ ] Ensure strong authorization system
  - [ ] Study up on the latest authorization best practices
  - [ ] Automated tests to ensure data integrity
  - [ ] Physical/logistical access controls should be in place (locking screens, not sharing passwords, etc)

- [ ] Make sure all cryptographic algorithms are up to date, like which sha algorithm which ECDSA curve, etc
- [ ] Rotate all keys (All current public and private keys, secrets, etc should be deleted and replaced by newly generated keys. Stripe keys, Twilio keys, GraphQL keys, Prisma keys, Rails keybase, etc should all be rotated.)
- [ ] Rotate all user passwords (All user passwords should be changed. They should be a minimum of 10 characters in length. GitLab, Gmail, AWS, Twilio, Cloud66, Stripe, Slack, etc.)
- [ ] Endpoints have proper authentication and authorization (All processes that are accessible through tcp/ip ports should be audited to ensure each endpoint has proper authentication and authorization. Analyze the types of operations, reads or writes, that are permitted. Any permitted operations should only allow access by those who need access.)
- [ ] Ensure physical integrity of all keys (Check that all keys can be physically accessed (for example, check USB drives to ensure the keys can be retrieved). Know where all keys are stored, check all laptops, USB drives, environment variable configs, safes, etc.)
- [ ] Review organizational access control policies (Review organizational access control policies such as who has access to what data, password length, password lifetimes, access to secret keys, password sharing, screen locking, proper data sharing channels (Gmail, Slack, Excel) etc)
- [ ] Sanitize data (Health data, credit card data, and other types of sensitive data with compliance requirements should never be stored in our systems anywhere, unless we can store them compliantly. If we are storing that data, we should track it down and delete it. We should also build the functionality to stop storing the data. Personal data should be deleted over time as it becomes unneeded.)
- [ ]  Revoke access to terminated employees (Review all user accounts. Anyone who is not currently an employee should be completely removed from our system so that they no longer have access to any sensitive data or functionality. Check our database, GitLab, Gmail, Twilio, Stripe, Slack, etc)
- [ ] Review compliance with regulations (Make sure we are compliant with HIPAA, PCI, GDPR, etc)
- [ ] Audit the audit (Take some time to study the latest security best practices. Ensure that our audit process is up-to-date and will lead to sufficient security. Clean up the issue, change wording, add audits, etc.)
- [ ] New audit to add: Ensure proper logging and monitoring. We don't really have a good way of knowing what attacks are taking place on our system, no alarms or anything to notify us of breaches
